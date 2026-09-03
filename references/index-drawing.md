# Class index: adsk.drawing

44 classes/enums found in `references/api-stubs/drawing.py`. Use `grep -n "^class ClassName" references/api-stubs/drawing.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `BaseDocumentTypes` |  | Specifies the base document option for drawing creation. |
| `CenterLineDisplayTypes` |  | Center line display options for cylindrical features. |
| `CenterMarkDisplayTypes` |  | Center mark display options for circular features. |
| `DefaultOriginTypes` |  | Default origin (datum) point for component dimension placement. |
| `DimensionStrategyTypes` |  | Dimension placement strategy for automatic dimensioning. |
| `DrawingContentTypes` |  | Specifies which assembly content is used when creating automatic drawing sheets (API supports |
| `DrawingCreationModes` |  | Specifies the mode of drawing creation. |
| `DrawingStandardTypes` |  | Specifies the different drawing standards that can be used. |
| `DrawingUnitTypes` |  | Specifies the different drawing units that can be used. |
| `DrawingViewStyleTypes` |  | Visual rendering style for drawing views. |
| `HolePreferencesTypes` |  | Hole and thread annotation preferences. |
| `PDFSheetsExport` |  | The various options that define which sheets to print. |
| `SheetCreationTypes` |  | Specifies which components get drawing sheets generated. |
| `SheetOrientationTypes` |  | Specifies the sheet orientation for printing and display. |
| `SheetSizes` |  | Specifies the sheet size for a drawing document. |
| `TableLocationTypes` |  | Corner location options for tables on sheets. Used for parts lists, bend tables, and other sheet tables. |
| `TangentEdgeDisplayTypes` |  | Tangent edge display options. |
| `AnimationPreferences` | core.Base | Preferences for animation/exploded view sheets. Enable via GlobalPreferences.generateAnimationSheet (default: false). |
| `AssemblyPreferences` | core.Base | Preferences for assembly sheets (main and sub-assembly). Includes ISO view, orthogonal views, and parts list options. |
| `AssemblySheetPreferences` | core.Base | Preferences for assembly sheet views (both ISO and orthogonal). Configure parts list and view sheet creation. |
| `AutoDimensionBasePreferences` | core.Base | Base auto-dimension settings: enable, strategy, hole preferences. |
| `AutomationPreferences` | core.Base | Central configuration hub for automatic drawing preferences. Access globalPreferences for sheet |
| `ComponentPreferences` | core.Base | Preferences for individual component (part) sheets with views, dimensions, and annotations. |
| `ComponentSheetViewPreferences` | core.Base | Preferences for component sheet views. Configure orthographic view creation and optional isometric view. |
| `CreateDrawingInput` | core.Base | Input parameters for drawing creation. Create via DrawingManager.createDrawingInput(). |
| `CustomSheetSize` | core.Base | Custom width and height cannot exceed 5000 mm × 5000 mm (millimeter units) or 200 inch × 200 inch (inch units). |
| `CustomTableInput` | core.Base | The input object that defines the required input to create a Custom table when using the |
| `CustomTables` | core.Base | Collection object that provides access to all custom tables on a sheet and supports creating new tables. |
| `DrawingExportManager` | core.Base | Provides support to export the drawing in various formats. |
| `DrawingExportOptions` | core.Base | The base class for the different drawing export types.  This class is never directly used |
| `DrawingManager` | core.Base | Application-level drawing functionality. Access via the static get property. |
| `DrawingViewPreferences` | core.Base | Drawing view appearance settings: style, edges, center marks, center lines. |
| `FlatPatternOrthogonalViewPreferences` | core.Base | Preferences for flat pattern orthogonal view sheets. Configure folded model view, bend table. |
| `FlatPatternPreferences` | core.Base | Preferences for sheet metal flat pattern sheets (unfolded state with bend information). |
| `FoldedModelPreferences` | core.Base | Preferences for sheet metal folded model sheets (formed state). Complements flat pattern sheets. |
| `GlobalPreferences` | core.Base | Global preferences for drawing generation: sheet toggles, auto-dimensioning, component omission. |
| `Sheet` | core.Base | Object that represents the sheet specific data within a drawing document. |
| `Table` | core.Base | Base class for all table objects in a drawing. |
| `AutoDimensionComponentPreferences` | AutoDimensionBasePreferences | Auto-dimension settings for components. Extends base with origin and pattern options. |
| `CustomTable` | Table | Represents a custom table on a drawing sheet. |
| `Drawing` | core.Product | Object that represents the drawing specific data within a drawing document. |
| `DrawingDocument` | core.Document | Object that represents a Fusion 360 drawing document. |
| `DrawingViewFlatPatternPreferences` | DrawingViewPreferences | Drawing view settings for flat patterns. Adds bend extents. Different defaults than base. |
| `PDFExportOptions` | DrawingExportOptions | Defines the inputs needed to export the drawing as PDF. |
