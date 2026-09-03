# Fusion scripting patterns

Verify any signature below against `references/api-stubs/core.py` if you're extending these — they're kept accurate as of the bundled stubs, but always re-check when you deviate from them.

## Scripts vs. add-ins vs. commands

- **Script**: one-shot. Fusion creates the file, imports it, calls `run(context)`, and (by default) tears the module down when `run` returns. Good for "do a thing once" tasks: batch-export bodies, generate a pattern of sketches, dump parameters to a CSV.
- **Add-in**: persistent. Fusion calls `run(context)` when the add-in is started and `stop(context)` when it's stopped (including on Fusion restart if the add-in is set to run on startup). Add-ins are how you add permanent UI (toolbar buttons, palettes) or things that must react to ongoing events. Needs a `.manifest` JSON file alongside the `.py` (autodesk-provided template — not part of the API itself, just tells Fusion how to load it).
- **Command**: not a separate file type — it's the UI object (`CommandDefinition` + a dialog) you create *inside* a script or add-in when the task needs user input (a dialog with fields) rather than running immediately. A script can create and execute a command; an add-in typically registers one on a toolbar panel.

### Minimal script

```python
import adsk.core, adsk.fusion, traceback

def run(context):
    ui = None
    try:
        app = adsk.core.Application.get()
        ui = app.userInterface

        design = adsk.fusion.Design.cast(app.activeProduct)
        if not design:
            ui.messageBox('No active Fusion design')
            return

        # ... do the work ...

    except:
        if ui:
            ui.messageBox('Failed:\n{}'.format(traceback.format_exc()))
```

Always wrap `run()` in `try/except` and report via `ui.messageBox(traceback.format_exc())`. There's no console attached to a running script by default, so an uncaught exception otherwise just silently aborts with nothing shown to the user — the single most common source of "my script doesn't do anything" reports. `traceback.format_exc()` gives the real Python traceback, which is far more useful for debugging than a generic message.

### Minimal add-in with a toolbar button and a command dialog

The critical rule here: **every event handler instance must be kept alive by a reference outside the function that creates it** (module-level list is simplest). Handlers are plain Python objects; if nothing holds a reference, Python garbage-collects them and the `notify` callback silently stops firing — Fusion gives no error, the command dialog just stops responding to input. This is the #1 subtle bug in generated add-in code.

```python
import adsk.core, adsk.fusion, traceback

app = adsk.core.Application.get()
ui = app.userInterface

_handlers = []          # keep every handler instance alive
CMD_ID = 'myAddinUniqueCmdId'
CMD_NAME = 'My Command'
CMD_TOOLTIP = 'Does a thing'
PANEL_ID = 'SolidCreatePanel'   # existing panel to add the button to

class MyCommandExecuteHandler(adsk.core.CommandEventHandler):
    def notify(self, args: adsk.core.CommandEventArgs):
        try:
            inputs = args.command.commandInputs
            value_input: adsk.core.ValueCommandInput = inputs.itemById('lengthInput')
            length = value_input.value   # internal units (cm)
            # ... use `length` to do the actual modeling work ...
        except:
            if ui:
                ui.messageBox('Execute failed:\n{}'.format(traceback.format_exc()))

class MyCommandCreatedHandler(adsk.core.CommandCreatedEventHandler):
    def notify(self, args: adsk.core.CommandCreatedEventArgs):
        try:
            cmd = args.command
            inputs = cmd.commandInputs
            inputs.addValueInput('lengthInput', 'Length', 'mm',
                                  adsk.core.ValueInput.createByReal(1.0))

            on_execute = MyCommandExecuteHandler()
            cmd.execute.add(on_execute)
            _handlers.append(on_execute)
        except:
            if ui:
                ui.messageBox('CommandCreated failed:\n{}'.format(traceback.format_exc()))

def run(context):
    try:
        cmd_def = ui.commandDefinitions.itemById(CMD_ID)
        if not cmd_def:
            cmd_def = ui.commandDefinitions.addButtonDefinition(CMD_ID, CMD_NAME, CMD_TOOLTIP)

        on_created = MyCommandCreatedHandler()
        cmd_def.commandCreated.add(on_created)
        _handlers.append(on_created)

        panel = ui.allToolbarPanels.itemById(PANEL_ID)
        if not panel.controls.itemById(CMD_ID):
            panel.controls.addCommand(cmd_def)

    except:
        if ui:
            ui.messageBox('run failed:\n{}'.format(traceback.format_exc()))

def stop(context):
    try:
        cmd_def = ui.commandDefinitions.itemById(CMD_ID)
        if cmd_def:
            cmd_def.deleteMe()
        panel = ui.allToolbarPanels.itemById(PANEL_ID)
        ctrl = panel.controls.itemById(CMD_ID)
        if ctrl:
            ctrl.deleteMe()
    except:
        if ui:
            ui.messageBox('stop failed:\n{}'.format(traceback.format_exc()))
```

`stop()` cleaning up the `CommandDefinition` and toolbar control matters in practice: during development the user will Run/Stop the add-in repeatedly, and `addButtonDefinition` throws if a definition with that `id` already exists. Guard both directions (`itemById` check before creating, cleanup in `stop`).

Other command events worth knowing about — look each up in `core.py` (search `^class \w*EventHandler`) before using: `InputChangedEventHandler` (live dialog updates as the user edits fields — good for previews), `ValidateInputsEventHandler` (enable/disable OK button), `CommandEventHandler` used for both `execute` and `executePreview` (live 3D preview before commit), and `destroy` (dialog closed/canceled — clean up any preview geometry here).

## Error handling convention

Use `try/except:` (bare or `except Exception`) + `ui.messageBox(traceback.format_exc())` at every top-level entry point Fusion calls into (`run`, `stop`, every handler's `notify`). Each of these runs in a context where an uncaught exception has no other visible surface — it won't print to a terminal the user can see. Import `traceback` for this.

## Units

All lengths/values coming from and going to the geometry API (sketch dimensions, extrude distances, `Point3D` coordinates, etc.) are in **internal database units: centimeters and radians**, regardless of the document's or user's display unit settings. Two ways to handle user-facing units correctly:

1. `adsk.core.ValueInput.createByString('10 mm')` — lets Fusion parse a unit-qualified string (accepts any unit Fusion understands, including expressions), or `ValueInput.createByReal(x)` for a plain internal-units double.
2. `design.unitsManager.convert(value, fromUnit, toUnit)` and `design.unitsManager.evaluateExpression(expr, unitType)` for programmatic conversion, e.g. when reading a `ValueCommandInput` back in an execute handler (`.value` on a `ValueCommandInput` is already the evaluated internal-units double).

Don't assume a bare number the user gives you (e.g. "extrude 10mm") is already in the right unit before passing it to the API — either parse it via `ValueInput.createByString` or convert explicitly.

## Collections

Methods that take multiple entities (e.g. `Design.physicalProperties`, many CAM/pattern inputs) generally want an `adsk.core.ObjectCollection`, not a Python list:

```python
coll = adsk.core.ObjectCollection.create()
for body in bodies:
    coll.add(body)
```

Check the specific method's stub signature — some newer APIs accept a plain `list`, but a lot of the modeling API still requires `ObjectCollection`, and passing a list where it's not accepted fails with a type error at the API boundary rather than a helpful message.

## Casting

You'll see `SomeType.cast(obj)` throughout the stubs (e.g. `adsk.fusion.Design.cast(app.activeProduct)`). This is the standard pattern for narrowing a generically-typed return (`Product`, `Base`, etc.) to its concrete type before using type-specific members — `app.activeProduct` is typed as `Product` because it could be a `Design`, CAM `Document`, or other product type depending on the active workspace, so cast (and check for `None`) before assuming it's a `Design`.
