# Class index: adsk.electron

132 classes/enums found in `references/api-stubs/electron.py`. Use `grep -n "^class ClassName" references/api-stubs/electron.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `AttributeDisplayModes` |  | Visibility mode for attribute text. |
| `Caps` |  | Shape applied to the endpoints of an open stroke (wire or arc). |
| `DimensionTypes` |  | Measurement and annotation style for dimension objects. |
| `DrillSymbols` |  | Symbol used to annotate drill sizes in drill charts. |
| `ErrorStates` |  | Approval status of an error in the errors panel. |
| `ErrorTypes` |  | Severity or category of a design rule or electrical rule check error. |
| `FillPatterns` |  | Fill pattern used when displaying a layer. |
| `Fonts` |  | Rendering style for text (vector, proportional, or fixed). |
| `GateAddLevels` |  | When a gate is added when placing a multi-gate device (e.g., IC with multiple symbols). |
| `GridUnits` |  | Unit types for grid spacing and display. |
| `ObjectIdMode` |  | Object ID mode for queries. |
| `PadFlags` |  | Behavioral flags for through-hole pads. |
| `PadShapes` |  | Copper shape of a through-hole pad. |
| `PinDirections` |  | Electrical direction of a pin (input, output, power, etc.). |
| `PinFunctions` |  | Graphical symbol (inverter or clock) drawn next to a pin. |
| `PinLengths` |  | Graphical length of the pin wire in the symbol. |
| `PinVisibles` |  | Which name is displayed for the pin. |
| `PortBorderSides` |  | Side of the module symbol where a port is placed. |
| `PortDirections` |  | Signal flow direction for a port; used for ERC. |
| `RouteConnect` |  | How a contact reference connects when the element has multiple gates. |
| `SmdFlags` |  | Behavioral flags for SMD pads (stop mask, thermals, cream mask). |
| `TextAlignments` |  | Horizontal and vertical alignment of text relative to its anchor point. |
| `VerticalTextModes` |  | Orientation of vertically drawn text (upward or downward). |
| `ViaFlags` |  | Behavioral flags for a via (e.g., solder mask opening). |
| `ViaShapes` |  | Cross-section shape of a via. |
| `WireStyles` |  | Dash pattern applied to a wire stroke. |
| `Arc` | core.Base | Circular arc in a PCB board, schematic sheet, symbol, or package. |
| `Area` | core.Base | Rectangular bounding region defined by corner coordinates. |
| `Busses` | core.Base | The Busses collection provides access to all of the buses within a sheet or schematic. |
| `Circles` | core.Base | The Circles collection provides access to all of the circles within a board, sheet, symbol, or package. |
| `Class` | core.Base | Net class definition (design rules configuration); assigns trace width, drill, and other constraints. |
| `Classes` | core.Base | The Classes collection provides access to all of the net class definitions within a schematic or board. |
| `ContactRefs` | core.Base | The ContactRefs collection provides access to all of the contact references within a signal. |
| `Contacts` | core.Base | The Contacts collection provides access to all of the contacts (pads and SMDs) within a package. |
| `Devices` | core.Base | The Devices collection provides access to all of the devices within a device set. |
| `DeviceSets` | core.Base | The DeviceSets collection provides access to all of the device sets within a library. |
| `Dimensions` | core.Base | The Dimensions collection provides access to all of the dimensions within a board or sheet. |
| `EcadAttributes` | core.Base | The EcadAttributes collection provides access to all of the attributes within a parent object. |
| `EcadObject` | core.Base | Base class for all electronics design objects. |
| `ElectronicsExportManager` | core.Base | Manages export of an electronics document to various formats. |
| `ElectronicsExportOptions` | core.Base | Options that control how an electronics document is exported. |
| `ElectronManager` | core.Base | The main Electronics singleton. |
| `Elements` | core.Base | The Elements collection provides access to all of the elements within a board. |
| `Error` | core.Base | Single design rule check (DRC) or electrical rule check (ERC) error. |
| `Errors` | core.Base | The Errors collection provides access to all of the DRC or ERC errors within a board or schematic. |
| `Frames` | core.Base | The Frames collection provides access to all of the frames within a board or sheet. |
| `Gates` | core.Base | The Gates collection provides access to all of the gates within a device set. |
| `Grid` | core.Base | Represents the design grid settings for a board, schematic, or library. |
| `Holes` | core.Base | The Holes collection provides access to all of the through-holes within a board or package. |
| `Instances` | core.Base | The Instances collection provides access to all of the part instances within a schematic sheet. |
| `Junctions` | core.Base | The Junctions collection provides access to all of the junctions within a segment. |
| `Labels` | core.Base | The Labels collection provides access to all of the labels within a net, segment, or sheet. |
| `Layers` | core.Base | The Layers collection provides access to all of the layers within a board, schematic, or library. |
| `Libraries` | core.Base | The Libraries collection provides access to all of the libraries within a design (board or schematic). |
| `ModuleInstances` | core.Base | The ModuleInstances collection provides access to all of the module instances within a schematic or sheet. |
| `Modules` | core.Base | The Modules collection provides access to all of the modules within a schematic. |
| `Nets` | core.Base | The Nets collection provides access to all of the nets within a sheet or schematic. |
| `Packages` | core.Base | The Packages collection provides access to all of the packages (footprints) within a library. |
| `Packages3d` | core.Base | The Packages3d collection provides access to all of the 3D packages within a library or device. |
| `Pads` | core.Base | The Pads collection provides access to all of the pads within a package. |
| `Parts` | core.Base | The Parts collection provides access to all of the component definitions (parts) within a sheet or module. |
| `PinRefs` | core.Base | The PinRefs collection provides access to all of the pin references within a net segment. |
| `Pins` | core.Base | The Pins collection provides access to all of the pins within a symbol. |
| `PolyCutouts` | core.Base | The PolyCutouts collection provides access to all of the polygon cutouts within a board, symbol, or package. |
| `PolyPours` | core.Base | The PolyPours collection provides access to all of the copper pour polygons within a signal. |
| `PolyShapes` | core.Base | The PolyShapes collection provides access to all of the polygon shapes within a board, sheet, symbol, or package. |
| `PortInstances` | core.Base | The PortInstances collection provides access to port instances on a module instance. |
| `PortRefs` | core.Base | The PortRefs collection provides access to all of the port references within a net or segment. |
| `Ports` | core.Base | The Ports collection provides access to all of the ports within a module. |
| `Rectangles` | core.Base | The Rectangles collection provides access to all of the rectangles within a board, sheet, symbol, or package. |
| `Segments` | core.Base | The Segments collection provides access to all of the segments within a net or bus. |
| `Sheets` | core.Base | The Sheets collection provides access to all of the sheets within a schematic. |
| `Signals` | core.Base | The Signals collection provides access to all of the copper trace networks (signals) within a board. |
| `Smds` | core.Base | The Smds collection provides access to all of the SMD pads within a package. |
| `Splines` | core.Base | The Splines collection provides access to all of the splines within a board, sheet, symbol, or package. |
| `Symbols` | core.Base | The Symbols collection provides access to all of the symbols within a library. |
| `Technologies` | core.Base | The Technologies collection provides access to all of the technology variants within a device. |
| `Texts` | core.Base | The Texts collection provides access to all of the texts within a board, sheet, symbol, or package. |
| `Units` | core.Base | Static methods that convert internal units to physical units (mm, inch, mil, micron). |
| `VariantDefs` | core.Base | The VariantDefs collection provides access to all of the variant definitions within the schematic. |
| `Variants` | core.Base | The Variants collection provides access to all of the per-assembly-variant configurations for a part. |
| `Vias` | core.Base | The Vias collection provides access to all of the vias within a signal or board. |
| `Wires` | core.Base | The Wires collection provides access to all of the wires within a board, sheet, signal, or polygon. |
| `Bus` | EcadObject | Group of related nets in a schematic; wires can be drawn as a bus and named with a pattern to derive net names. |
| `Circle` | EcadObject | Circle primitive drawn on a PCB board, schematic sheet, symbol, or package. |
| `Contact` | EcadObject | Contact point (pad or SMD) in a package that connects to a signal. |
| `ContactRef` | EcadObject | Reference connecting a signal to a pad or SMD on a placed component. |
| `Device` | EcadObject | Package variant within a device set; combines a symbol configuration with a specific package. |
| `DeviceSet` | EcadObject | Definition of a device set in a library. Groups devices with different packages but the same symbol and gate configuration. |
| `Dimension` | EcadObject | Dimension annotation on a PCB board or schematic sheet that displays measured distances, angles, or radius. |
| `EcadAttribute` | EcadObject | Attribute (name-value pair) on an element, instance, or part. |
| `EcadDocument` | core.Product | Base class for electronics design documents that can be opened in the application (design, schematic, board, library). |
| `Element` | EcadObject | Placed component instance on a PCB. |
| `Frame` | EcadObject | Frame element (drawing border or title block) on a board or sheet. |
| `Gate` | EcadObject | Gate (logical sub-unit) within a device; references a symbol and defines placement and add behavior. |
| `Hole` | EcadObject | Non-plated through-hole drill in a PCB board or package. |
| `Instance` | EcadObject | Placed part instance (component reference) on a schematic sheet. |
| `Junction` | EcadObject | Connection point where two or more net wires meet on a schematic sheet. |
| `Label` | EcadObject | Label (net name annotation) on a schematic sheet, net, or bus. |
| `Layer` | EcadObject | Layer in a board, schematic, or library. |
| `Module` | EcadObject | Reusable block in a hierarchical schematic, containing parts, ports, and nested sheets. |
| `ModuleInstance` | EcadObject | Placed reference to a module on a schematic sheet. |
| `Net` | EcadObject | Logical connection (net) in a schematic; groups pins and ports that are electrically connected. |
| `Package` | EcadObject | Footprint definition in a library; defines pad layout and silk screen for PCB placement. |
| `Package3d` | EcadObject | 3D model definition in a library; can be attached to footprints for 3D board visualization. |
| `Pad` | EcadObject | Through-hole pad in a package. |
| `Part` | EcadObject | Component definition in a schematic sheet or module; has a name, value, and references a device. |
| `Pin` | EcadObject | Electrical connection point in a symbol; defines position, direction, and display. |
| `PinRef` | EcadObject | Reference linking an instance, part, and pin in a net segment. |
| `PolyCutout` | EcadObject | Polygon cutout region that subtracts from signal polygons in the same layer. |
| `PolyPour` | EcadObject | Copper pour polygon belonging to a signal; filled (solid or hatched) copper area. |
| `PolyShape` | EcadObject | Simple polygon shape on a board, schematic sheet, symbol, or package; no copper fill. |
| `Port` | EcadObject | Connection point that exports a net from a module to the outside; defines the interface for hierarchical schematics. |
| `PortInstance` | EcadObject | Graphical port instance on a placed module instance (distinct from the logical Port definition). |
| `PortRef` | EcadObject | Reference that connects a net to a port on a module instance. |
| `Rectangle` | EcadObject | Rectangle primitive drawn on a PCB board, schematic sheet, symbol, or package. |
| `Segment` | EcadObject | Wire segment group within a net or bus; connects pin references, port references, and wires. |
| `Sheet` | EcadObject | Represents one page of a multi-sheet schematic. |
| `Signal` | EcadObject | Copper trace network in a PCB board; connects pads and vias through wires and polygon pours. |
| `Smd` | EcadObject | Surface-mount (SMD) pad in a package. |
| `Spline` | EcadObject | Spline curve on a PCB board, schematic sheet, symbol, or package. |
| `Symbol` | EcadObject | Schematic symbol definition from a library; contains pins, wires, circles, and other graphic primitives. |
| `Technology` | EcadObject | Technology variant of a device; each variant has a name and technology-specific attributes. |
| `Text` | EcadObject | Text annotation on a PCB board, schematic sheet, symbol, or package. |
| `Variant` | EcadObject | Per-assembly-variant configuration of a part; specifies populate, technology, and value for one variant definition. |
| `VariantDef` | EcadObject | Assembly or build variant that controls which parts are populated in a schematic or board. |
| `Via` | EcadObject | Plated through-hole or blind/buried via connecting layers in a PCB board. |
| `Wire` | EcadObject | Straight or curved line segment in a PCB board, schematic sheet, symbol, or package. |
| `Board` | EcadDocument | Represents a PCB in an electronics design. Provides access to elements, signals, layers, and design-rule checks. |
| `EcadDesign` | EcadDocument | Represents an electronics design that contains both schematic and board representations. |
| `Library` | EcadDocument | Represents a library document in an electronics design. |
| `Schematic` | EcadDocument | Represents a schematic in an electronics design. |
