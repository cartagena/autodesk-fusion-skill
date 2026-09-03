# Common parametric-modeling workflows

All snippets below have their class/method names checked against `references/api-stubs/{core,fusion}.py`. Line numbers will drift as you look things up yourself — always re-grep rather than trusting a remembered line number. Treat these as verified starting points, not a substitute for checking a method's full docstring when you're using options not shown here (every method has far more optional parameters/behavior documented in its stub than fits here).

## Getting the active design

```python
app = adsk.core.Application.get()
ui = app.userInterface
design = adsk.fusion.Design.cast(app.activeProduct)   # None if active doc isn't a design (e.g. CAM/drawing)
root = design.rootComponent
```

`app.activeProduct` is typed as `Product` because Fusion documents can host different product types (`Design`, CAM, drawing...); always `cast` and check for `None` before using `Design`-only members.

## Components and occurrences

- `Component` = the definition (geometry, sketches, features). `Occurrence` = an instance of a component placed in a parent component's context (has its own transform). The root component (`design.rootComponent`) is itself a `Component`, not an `Occurrence`.
- `root.occurrences` → `Occurrences` collection. `root.occurrences.addNewComponent(transform: adsk.core.Matrix3D)` creates a brand-new empty component and returns the `Occurrence` referencing it; get the new `Component` via `occurrence.component`.
- Walk the whole assembly with `root.allOccurrences` (flattened, includes nested) vs `root.occurrences` (direct children only).

```python
transform = adsk.core.Matrix3D.create()   # identity
occ = root.occurrences.addNewComponent(transform)
new_comp = occ.component
new_comp.name = 'Bracket'
```

## Sketch + profile + extrude

```python
sketches = root.sketches
xy_plane = root.xYConstructionPlane
sketch = sketches.add(xy_plane)             # Sketches.add(planarEntity, occurrenceForCreation=None) -> Sketch

lines = sketch.sketchCurves.sketchLines
p1 = adsk.core.Point3D.create(0, 0, 0)
p2 = adsk.core.Point3D.create(5, 3, 0)      # internal units: cm
lines.addTwoPointRectangle(p1, p2)

profile = sketch.profiles.item(0)           # Profiles collection populated automatically from closed loops

extrudes = root.features.extrudeFeatures
distance = adsk.core.ValueInput.createByString('10 mm')
ext_input = extrudes.createInput(profile, adsk.fusion.FeatureOperations.NewBodyFeatureOperation)
ext_input.setDistanceExtent(False, distance)   # isSymmetric, distance -- check ExtrudeFeatureInput stub for other extents (ToEntity, TwoSides, etc.)
extrude = extrudes.add(ext_input)
```

For a quick one-liner extrude without configuring taper/direction/extents, `extrudes.addSimple(profile, distance: ValueInput, operation: FeatureOperations)` skips the create-input step. Use `createInput`/`add` whenever you need to set anything beyond a straight single-direction distance (symmetric, two-sided, to-object, taper angle, etc.) — check `ExtrudeFeatureInput`'s full member list in the stub, since it has many setters (`setOneSideExtent`, `setTwoSidesExtent`, `setSymmetricExtent`, `taperAngle`, `startExtent`, ...).

`FeatureOperations` (an enum-like class in `fusion.py`) has: `JoinFeatureOperation`, `CutFeatureOperation`, `IntersectFeatureOperation`, `NewBodyFeatureOperation`, `NewComponentFeatureOperation` — grep it for the exact list before using one you're not sure of.

Other feature-creation collections follow the same create-input/add (and often addSimple) shape: `root.features.revolveFeatures`, `.sweepFeatures`, `.loftFeatures`, `.filletFeatures`, `.chamferFeatures`, `.shellFeatures`, `.rectangularPatternFeatures`, `.circularPatternFeatures`, `.mirrorFeatures`, `.holeFeatures`, `.combineFeatures`. Grep `^class \w*FeatureInput\b` and `^class \w*Features\b` in `fusion.py` for the one you need — don't assume method names transfer exactly between feature types (e.g. some take a `ObjectCollection` of profiles, some take a single `Profile` or `Path`).

## Parameters (user parameters / model parameters)

```python
user_params = design.userParameters
length_param = user_params.add(
    'Length',
    adsk.core.ValueInput.createByReal(5.0),   # interpreted in the internal unit for "units" below
    'cm',
    'overall bracket length'
)

# Read/update later:
p = user_params.itemByName('Length')
p.expression = '7.5 cm'      # setting .expression re-evaluates and updates the model
```

Model (feature-driven) dimensions are exposed via `design.allParameters` or a specific feature's `.dimensions`/relevant properties — user parameters (`design.userParameters`) are the ones you create explicitly for driving the design externally (e.g. from a script that iterates configurations).

## Timeline (history) and rollback

`design.timeline` is a `Timeline` collection of `TimelineObject`s (one per feature/sketch/etc. in creation order). Useful members: `timeline.item(index)`, `timelineObject.rollTo(rollBefore: bool)` to move the design's rollback marker (e.g. to suppress everything after a point), `timelineObject.deleteMe()`, `timeline.moveToBeginning()`/similar. Grep `^class Timeline\b` and `^class TimelineObject\b` in `fusion.py` before scripting timeline manipulation — rollback state affects what geometry/features are currently valid to reference.

## Export

```python
export_mgr = design.exportManager
# STEP:
step_options = export_mgr.createSTEPExportOptions('C:/path/to/output.step', root)  # geometry arg optional -> whole design
export_mgr.execute(step_options)
# STL:
stl_options = export_mgr.createSTLExportOptions(root, 'C:/path/to/output.stl')  # check exact arg order in stub, it differs by format
export_mgr.execute(stl_options)
```

Every `create*ExportOptions` method (`createIGESExportOptions`, `createSTEPExportOptions`, `createSTLExportOptions`, `createSATExportOptions`, `createFusionArchiveExportOptions`, ...) has its own argument order and options object — grep `^class ExportManager\b` in `fusion.py` and read each one's docstring rather than assuming they match; some take `(filename, geometry)`, others `(geometry, filename)` or have format-specific settings objects (mesh refinement for STL, etc.).

## Selections and ObjectCollection

```python
coll = adsk.core.ObjectCollection.create()
for body in root.bRepBodies:
    coll.add(body)
props = design.physicalProperties(coll)  # example consumer that wants a collection, not a list
```

Interactive selection (asking the user to pick something) uses `ui.selectEntity(prompt, filter)` for a single pick outside a command dialog, or a `SelectionCommandInput` (`commandInputs.addSelectionInput(...)`) inside a command dialog for multi-select with live filtering — grep `^class SelectionCommandInput\b` in `core.py` for `.setSelectionLimits` / `.addSelectionFilter` details.

## Events beyond command dialogs

If the task is "react to something happening in Fusion" rather than "run once" or "show a dialog," look at `app.documentSaving`, `app.documentSaved`, `app.documentActivated`, `ui.commandStarting`/`ui.commandTerminated`, and workspace/panel events — all on `Application`/`UserInterface` in `core.py` (grep `Event$` properties on those two classes). Same lifetime rule as command handlers: keep the handler instance referenced (module-level list) for the life of the add-in.

## Non-parametric domains

These live in the other modules — see `references/module-map.md` for which file/index to check first:
- **CAM/toolpaths** (`adsk.cam`): setups, operations (`Adaptive2dOperation`, `Pocket2dOperation`, etc.), tool libraries, post-processing/NC output.
- **Drawings** (`adsk.drawing`): drawing documents, views, dimensions, annotations, sheets/borders.
- **Electronics/PCB** (`adsk.electron`): schematic and PCB design, nets, footprints, traces.
- **Simulation** (`adsk.sim`): studies, constraints, contacts, loads, meshing, results.
- **Volume/lattice** (`adsk.volume`): volumetric/graph-based lattice and implicit modeling (newer, marked preview in many classes).
