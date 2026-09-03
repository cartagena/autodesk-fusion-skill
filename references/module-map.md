# Module map

Fusion's Python API is split across 8 files (7 `adsk.*` submodules plus the `adsk` package root). Import only what you need — `adsk.core` and `adsk.fusion` cover the overwhelming majority of scripts.

| Module | Stub file | Index | Classes | What it's for | Import |
|---|---|---|---|---|---|
| `adsk` (root) | `api-stubs/__init__.py` | — | 3 functions | Script lifecycle utilities: `terminate()`, `autoTerminate(bool)`, `doEvents()`. Tiny — read the file directly, no index needed. | `import adsk` |
| `adsk.core` | `api-stubs/core.py` | `index-core.md` | 343 | Application/UI framework shared by everything else: `Application`, `UserInterface`, `Document`, `Product`, command dialogs & inputs, events/event handlers, geometry primitives (`Point3D`, `Vector3D`, `Matrix3D`, `ObjectCollection`), `ValueInput`, materials/appearances, selection. Almost every script touches this. | `import adsk.core` |
| `adsk.fusion` | `api-stubs/fusion.py` | `index-fusion.md` | 903 | The parametric design data model: `Design`, `Component`, `Occurrence`, sketches (`Sketch`, `SketchCurves`, `Profile`), all solid/surface features (`ExtrudeFeatures`, `RevolveFeatures`, ...), the `Timeline`, parameters, `BRepBody`/`BRepFace`/`BRepEdge`, joints, `ExportManager`. This is the biggest module and where most "model something" tasks live. | `import adsk.fusion` |
| `adsk.cam` | `api-stubs/cam.py` | `index-cam.md` | 229 | CAM/manufacturing: `CAM` (the product, like `Design` is for modeling), `Setups`/`Setup`, `Operations`/`Operation` (2D/3D milling, turning, additive strategies), tool libraries, post-processing to NC code, `CAMManager`. Depends on `adsk.fusion` for the geometry being machined. | `import adsk.cam` |
| `adsk.drawing` | `api-stubs/drawing.py` | `index-drawing.md` | 44 | 2D drawing documents: `DrawingDocument`, `Sheet`/`Sheets`, drawing views, dimensions/annotations, title blocks. Small module — depends on `adsk.core`. | `import adsk.drawing` |
| `adsk.electron` | `api-stubs/electron.py` | `index-electron.md` | 132 | Electronics/PCB design: `EcadDocument` and its specializations `Board`, `Schematic`, `EcadDesign`, `Library` — nets, footprints, traces, layers. Depends on `adsk.core` and `adsk.fusion` (boards relate to 3D geometry). | `import adsk.electron` |
| `adsk.sim` | `api-stubs/sim.py` | `index-sim.md` | 64 | Simulation studies: `Study`, `SimulationModel(s)`, constraints, contacts, loads, materials for FEA-style analysis. Many classes marked preview/warning in their docstrings — check for that warning before relying on stability. Depends on `adsk.core`/`adsk.fusion`. | `import adsk.sim` |
| `adsk.volume` | `api-stubs/volume.py` | `index-volume.md` | 30 | Volumetric/graph-based lattice and implicit modeling — a node-graph system (`Graph`, `GraphNode`, `GraphConnector`, typed `GraphNodeProperty` subclasses). Newest and smallest module; most classes are marked preview. Depends on `adsk.core`/`adsk.fusion`. | `import adsk.volume` |

## Picking the right module for a task

- "Create/modify geometry, sketches, features, components, assemblies, parameters, export a model" → `adsk.core` + `adsk.fusion`.
- "Generate toolpaths, set up a CAM job, post to G-code" → add `adsk.cam` (still needs `adsk.fusion` for the part geometry and `adsk.core` for the app/UI).
- "Create or edit a 2D drawing / drawing views / dimension a drawing" → add `adsk.drawing`.
- "PCB layout, schematic, nets, footprints" → add `adsk.electron`.
- "Set up or run a structural/thermal simulation study" → add `adsk.sim`.
- "Lattice structures, implicit/volumetric modeling, TPMS-style infill" → add `adsk.volume`.
- Command dialogs, toolbar UI, events, selection, units, geometry math — always `adsk.core`, regardless of domain.

## Warning markers in the stubs

Many docstrings across `cam.py`, `drawing.py`, `electron.py`, `sim.py`, and `volume.py` (and some in `fusion.py`) start with:

```
!!!!! Warning !!!!!
! This is in preview state; please see the help for more info
!!!!! Warning !!!!!
```

That's Autodesk's own marker for API surface that's newer/less stable and more likely to change between Fusion releases, or to require a specific preview feature flag to be enabled in the user's Fusion install. Flag this to the user when a workflow depends heavily on preview-marked classes — the code may work today and break after a Fusion update, or may not be available at all if the user doesn't have the relevant preview toggle on.
