---
name: autodesk-fusion-api
description: Reference and workflow guide for writing Autodesk Fusion (Fusion 360) Python scripts and add-ins using adsk.core, adsk.fusion, adsk.cam, adsk.drawing, adsk.electron, adsk.sim, and adsk.volume. Use whenever the user wants to write, debug, or explain a Fusion Python script or add-in — parametric modeling (sketches, features, components, timeline, parameters), CAM/toolpaths, drawings, PCB/electronics, simulation studies, lattice/volume modeling, command dialogs/event handlers, or any Fusion UI/API automation. Also trigger on terms like "adsk.core", "adsk.fusion", "rootComponent", "ExtrudeFeatures", "CommandCreatedEventHandler", or "Fusion add-in", even without a file type named. Bundles the actual current Fusion API class stubs as ground truth, so consult it instead of relying on memory for exact method/property names — the API is huge, versioned, and easy to misremember.
---

# Fusion 360 Python API

Fusion's Python API is enormous (~1,750 classes across 7 modules). Nobody — including you — reliably remembers exact method signatures, parameter names, enum values, or which class owns which property. **Ground truth for this skill is the bundled API stub files in `references/api-stubs/`.** They're auto-generated directly from the current Fusion API for code-intellisense purposes, so they're authoritative even where they conflict with your training data or the public docs (which lag behind releases).

The working rule for this whole skill: **before writing a call to any Fusion API class/method/property you're not 100% sure of, grep it in the stubs.** This isn't optional busywork — Fusion scripts fail silently or throw opaque `RuntimeError`s at the `ui.messageBox` catch-all when a method name, arg order, or enum value is wrong, and there's no local Fusion install to test against in this environment. Getting the signature right the first time from the stub is much cheaper than guessing and iterating with the user.

## How to look things up

The stub files are large (fusion.py alone is ~2.8MB / 63k lines), so never `view` or `cat` a whole one. Search instead:

```bash
# Find a class definition and read just it (class blocks are not indented at top level,
# so the next "^class " line marks the end)
grep -n "^class ExtrudeFeatureInput" references/api-stubs/fusion.py
sed -n '14768,15079p' references/api-stubs/fusion.py   # from that line to the next class

# Find which module a class lives in when you're not sure
grep -rln "^class Sketches\b" references/api-stubs/*.py

# List all methods/properties defined on a class you've already located
sed -n '<start>,<end>p' references/api-stubs/<file>.py | grep -n "def \|@property"

# Search for a method name across all modules
grep -rn "def createInput" references/api-stubs/*.py
```

Each `references/index-<module>.md` file is a browsable table of contents (class name, base class, one-line summary) for that module — read the relevant one first when you're not sure which class you need, then grep the stub file for the full definition. `references/module-map.md` explains what each of the 7 modules covers so you know which index to check.

The stub docstrings are unusually thorough — full parameter descriptions, return value semantics, and usage notes are typically included. Read the whole docstring, not just the signature; Fusion methods have real gotchas (units are always internal cm/radians unless you use `ValueInput`, collections need `ObjectCollection`, many "create" calls are two-step create-input-then-add, etc.).

## Before writing any code

1. **Clarify script vs. add-in vs. command** if it's not obvious (see `references/scripting-patterns.md`). This changes the boilerplate significantly.
2. **Identify which module(s) you need.** Most parametric-modeling tasks live entirely in `adsk.core` + `adsk.fusion`. Only pull in `adsk.cam`, `adsk.drawing`, `adsk.electron`, `adsk.sim`, or `adsk.volume` if the task is actually about that domain — check `references/module-map.md`.
3. **Look up every non-trivial class/method you plan to call** using the grep workflow above before writing the line that uses it. Don't skip this because a name "looks right" — Fusion has many near-miss names (e.g. `Sketch` vs `Sketches`, `Component` vs `Occurrence`, `Profile` vs `Profiles`, `addSimple` vs `createInput`/`add`) and getting it wrong wastes the user's time debugging inside Fusion.
4. **Read `references/scripting-patterns.md`** for the boilerplate, event-handling lifetime rules, and error-handling convention — these are easy to get subtly wrong (e.g. losing event handler references to garbage collection) and the failure mode is confusing.

## Writing the script

Use `references/scripting-patterns.md` for:
- Script vs. add-in entry point structure (`run`/`stop`, `autoTerminate`)
- The standard `try/except` + `ui.messageBox(traceback.format_exc())` error-handling pattern (use this — silent failures in Fusion are painful to debug otherwise)
- Command dialogs: `CommandDefinition`, `CommandCreatedEventHandler`, input creation, `CommandEventHandler` for `execute`/`inputChanged`/`validateInputs`, and **why handler objects must be kept alive** (stored in a module-level list) or they'll be garbage collected and silently stop firing
- Units: internal values are always cm/radians; use `adsk.core.ValueInput` or the design's `unitsManager` to convert user-facing units

Use `references/workflows.md` for worked, verified-against-the-stubs examples of common tasks: getting the active design, walking components/occurrences, creating a sketch and profile, extrude/revolve/sweep/pattern features, working with parameters and the timeline, and exporting.

Use `references/module-map.md` to route CAM, drawing, electronics (PCB), simulation, or lattice/volume-modeling tasks to the right classes.

## After writing the code

- Reread it against the actual stub signatures you looked up — check argument order and types (many Fusion methods take an `ObjectCollection` or a specific enum, not a plain list or string).
- Make sure every `CommandCreatedEventHandler`/`InputChangedEventHandler`/etc. instance is assigned to a variable that's appended to a persistent list (see `references/scripting-patterns.md`) — this is the single most common bug in generated Fusion add-in code.
- Wrap the top-level `run(context)` body in the standard try/except so failures surface a message box instead of failing silently.
- If the script is an add-in with a command dialog, make sure `stop(context)` cleans up the command definition and removes UI controls it added, or repeated Run/Stop cycles during development will error on "already exists."

## Scope note

This skill is about the **Fusion Python API** for scripts/add-ins running inside Fusion (`adsk.core`/`adsk.fusion`/etc.), not the separate Fusion (Forge/APS) cloud REST API, and not Fusion's UI usage as an end user. If the user's request is about the cloud Data Management / Design Automation REST APIs instead, say so — that's a different SDK with different auth and object model, not covered by these stubs.
