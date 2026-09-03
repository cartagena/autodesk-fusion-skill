# Class index: adsk.cam

229 classes/enums found in `references/api-stubs/cam.py`. Use `grep -n "^class ClassName" references/api-stubs/cam.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `AdditiveFEAAnalysisType` |  | The valid analysis types for an additive FEA simulation. |
| `AdditiveFEACard` |  | The valid keyword card names for an AdditiveFEADeckBuilderCard in an AdditiveFEADeckBuilder.  Any cards not in this enum can still be made u |
| `AdditiveFEAGenerationType` |  | The valid generation types for an additive FEA simulation. |
| `AdditiveFEAMaterial` |  | The valid materials for PRM generation.  For subsequent part scale models, material properties are automatically loaded from the PRM file. |
| `AdditiveFEAPowderType` |  | The valid types for the PowderTypeCard. |
| `AdditiveFEASTLConfiguration` |  | The STL configuration IDs for the *STLM card. |
| `AdditiveTechnologies` |  | List of technologies a additive machine could have |
| `ArrangePriorityTypes` |  | Enum for the types of priority for an arrange selection. |
| `AutomaticGenerationModes` |  | Defines the automatic generation during the creation of an operation using OperationInput or createFromCAMTemplate2. |
| `CAM3MFSupportInclusionType` |  | Sets how the support should be included into the 3mf |
| `CAMAdditiveContainerTypes` |  | Enum specifying the types of additive containers available in Fusion. |
| `DefaultGroupType` |  | Types of default groups. Used to specify which default group to be retrieved by defaultGroup method. |
| `ExtensionMethods` |  | Enum for the types of extension methods for a chain selection. It defines how open curves are extended on their open end. |
| `ExtensionTypes` |  | Enum for types of extension capping. |
| `FloatParameterValueTypes` |  | Defines the type of a FloatParameterValue. |
| `FusionHubExecutionBehaviors` |  | Enum to define the behavior when posting to Fusion hub. |
| `GeneratedDataType` |  | Enum for the identifiers of generated results an OperationBase object can have |
| `HoleSegmentType` |  | Represents the recognized geometric shape of a hole segment. |
| `LibraryLocations` |  | List of locations representing folders in the library dialogs. |
| `LoopTypes` |  | Enum to define the type of loop for a face contour selection. |
| `MachineAnglePreferences` |  | Preference for rotary axis starting angles. |
| `MachineAxisCoordinates` |  | Options to control which coordinate is used for post processing, independent of the axis direction. |
| `MachineAxisTypes` |  | List of machine axis types for MachineAxis |
| `MachineCoolant` |  | Enumeration of possible coolants that a machine can use. |
| `MachineElementInputType` |  | Enumeration of the types of machine element inputs that can be created. |
| `MachineItemType` |  | Enumeration of possible MachineItem types. |
| `MachineNonTCPInterpolationMode` |  | Interpolation modes available for non-TCP motions. |
| `MachinePartTypes` |  | List of part types for MachinePart |
| `MachineResetOptions` |  | Axis reset preference options for MachineAxisConfiguration.whenToReset. |
| `MachineTCPInterpolationMode` |  | Interpolation modes available for TCP motions. |
| `MachineTemplate` |  | List of the machine templates to create a machine from. |
| `MachiningMode` |  | Specifies how to treat a surface group |
| `ModifyUtilityTypes` |  | Types of provided ModifyUtility. |
| `MultiAxisDegreesPerMinuteType` |  | Enumeration of the multi-axis degrees per minute types that can be used in MultiAxisDPMFeedrateSettings and its specializations. |
| `MultiAxisFeedMode` |  | Enumeration of the multi-axis feed modes that can be used in MultiAxisFeedrateSettings and its specializations. |
| `MultiAxisInverseTimeUnit` |  | The time unit used to calculate the feedrate for the MultiAxisInverseTimeFeedrateSettings |
| `MultiAxisRetractPreference` |  | Enumeration of the multi-axis retract preferences that can be used in MultiAxisRetractAndReconfigureSettings. |
| `MultiAxisRewindPreference` |  | Enumeration of the multi-axis rewind preferences that can be used in MultiAxisRetractAndReconfigureSettings. |
| `MultiAxisRotationTypes` |  | Enum for the types of multi-axis rotation for an arrange selection. |
| `MultiAxisSingularityLinearizeMethod` |  | The linearization method the MultiAxisSingularitySettings should use. |
| `NoteIconColors` |  | Available colors for the note icon. |
| `OperationStates` |  | The possible states of an operation. Some operations do not generate toolpaths, their state ignores the potential toolpath states. |
| `OperationTypes` |  | The valid options for the Operation Type of a Setup. |
| `PostCapabilities` |  | List of capabilities a post configuration can support. |
| `PostOutputUnitOptions` |  | List of the valid options for the outputUnit property on a PostProcessInput object . |
| `PostProcessExecutionBehaviors` |  |  |
| `PrintSettingItemTypes` |  | Enum that represents the types of CAMParameters. |
| `RecognizedPocketBottomType` |  | Types of pocket bottoms that can exist. Flat represents a standard flat bottom with sharp |
| `SetupChangeEventType` |  | List of setup change event types. |
| `SetupSheetFormats` |  | List of the formats to choose from when generating setup sheets |
| `SetupStockModes` |  | List of setup stock modes. |
| `SideTypes` |  | Enum for the order of loops. |
| `SplitSupportTypes` |  | Split support behavior depending on the type of support. |
| `ToolJointType` |  | Identifies the type of joint origin for tool assembly components. |
| `AdditiveFEAConvection` | core.Base | Convection defines the temperature-dependent heat loss boundary condition according to Newton's law of cooling. |
| `AdditiveFEADeckBuilder` | core.Base | The AdditiveFEADeckBuilder supplies methods to generate cards to be used for generating an FEA simulation result. |
| `AdditiveFEADeckBuilderCard` | core.Base | An AdditiveFEADeckBuilderCard is a single card in an additive FEA simulation input file. |
| `AdditiveFEASTLMap` | core.Base | The AdditiveFEASTLMap defines the relationship of geometries in STL format to parts, supports, materials, PRM files, and volume fractions or |
| `ArrangeSelections` | core.Base | Collection for all arrange selections to be passed to a CAMArrangeParameterValue object. |
| `AssemblyComponentGeometry` | core.Base | Represents the 3D geometry and attachment points for a tool component (such as a tool holder or tool block). |
| `CAM3MFExportMetadataOptions` | core.Base | Class providing read and write access to meta data of a 3MF file. |
| `CAM3MFExportStructure` | core.Base | Options for the 3MF structure and naming conventions. |
| `CAMAdditiveBuildExportFilter` | core.Base | Export filter used by CAMAdditiveMachineBuildFileExportOptions. |
| `CAMExportFuture` | core.Base | Used to check the state and get back the results of an operation generation. |
| `CAMExportManager` | core.Base | Export manager used to export the setup's models in one of the formats defined the ExportOptions objects. |
| `CAMExportOptions` | core.Base | Parent class for all ExportOptions objects giving access to the setup and file name used for the export. |
| `CAMFolders` | core.Base | Collection that provides access to the folders within an existing setup, folder or pattern. |
| `CAMLibrary` | core.Base | The CAMLibrary is the base-class for all other asset-specific libraries. |
| `CAMLibraryManager` | core.Base | CAMLibraryManager provides access to properties related to various libraries in the |
| `CAMManager` | core.Base | This singleton object provides access to application-level events and properties |
| `CAMParameter` | core.Base | Base class for representing parameter of an operation. |
| `CAMParameters` | core.Base | Collection that provides access to the parameters of an existing operation. |
| `CAMPatterns` | core.Base | Collection that provides access to the patterns within an existing setup, folder or pattern. |
| `CAMTemplate` | core.Base | Object that represents a template for a set of operations. These can be created from operations, |
| `CAMTemplateOperationInput` | core.Base | A CAMTemplateOperationInput provides access to Operation Template parameters for editing, in much the same way as |
| `CAMTemplateOperations` | core.Base | A list of CAMTemplateOperationInput. |
| `ChildOperationList` | core.Base | Provides access to the collection of child operations, folders and patterns of an existing setup. |
| `CreateFromCAMTemplateInput` | core.Base | Object that contains the settings used by createFromCAMTemplate. |
| `CurveSelections` | core.Base | Collection for all curve selections to be passed to a CadContours2DParameterValue object. |
| `DocumentStockMaterialLibrary` | core.Base | DocumentStockMaterialLibrary provides access to stock materials used by the document. |
| `GeneratedData` | core.Base | Parent class of all generated data classes. Acts like a void pointer for the entries in the OperationBase.GeneratedDataCollection property. |
| `GeneratedDataCollection` | core.Base | Collection can hold multiple GeneratedData results for a particular operation, setup or folder. |
| `GenerateToolpathFuture` | core.Base | Used to check the state and get back the results of an operation generation. |
| `GeometrySelection` | core.Base | Base parent class for all selection classes. All selections are currently restricted to B-Rep entities or sketches. |
| `Machine` | core.Base | Object that represents a machine. |
| `MachineAvoidGroups` | core.Base | Collection of all the mutually exclusive surface groups to be passed to a toolpath with stock to leave and avoid clearances associated to th |
| `MachineAxis` | core.Base | Abstract base class representing a single machine axis. |
| `MachineAxisConfiguration` | core.Base | MachineAxisConfiguration holds controller settings that differ for each axis. |
| `MachineAxisConfigurations` | core.Base | Collection of axis configuration objects. |
| `MachineAxisInput` | core.Base | Object that defines the properties required to create a machine axis object. |
| `MachineAxisRange` | core.Base | Class representing limits of motion for a machine axis. |
| `MachineCapabilities` | core.Base | Object that represents the capabilities of the machine. |
| `MachineElement` | core.Base | Base class for objects that compose a machine. |
| `MachineElementInput` | core.Base | Base class for machine element inputs. |
| `MachineElements` | core.Base | Collection of machine elements. |
| `MachineInput` | core.Base | Base abstract class for inputs to be used when creating machines. |
| `MachineInteractionPair` | core.Base | MachineInteractionPair objects control how a pair of MachineItems interact with each other. |
| `MachineItem` | core.Base | An item on a machine that can collide. |
| `MachinePart` | core.Base | Object representing some part of a machine, such as the static base of the machine, an |
| `MachinePartInput` | core.Base | Object representing the set of inputs required to create a new MachinePart. |
| `MachineParts` | core.Base | Object that represents a collection of machine parts. |
| `MachineQuery` | core.Base | MachineQuery defines the query to access Machines. |
| `MachineSpindle` | core.Base | Object representing a spindle on the machine |
| `MachineSpindleInput` | core.Base | Object representing the set of inputs required to create a new MachineSpindle. |
| `MachineToolStation` | core.Base | Object representing a tool station on the machine |
| `MachineToolStationInput` | core.Base | Object representing the set of inputs required to create a new MachineToolStation. |
| `MachiningTime` | core.Base | Object returned when using the getMachiningTime method from the CAM class. |
| `ManufacturingModel` | core.Base | Represents a ManufacturingModel within a CAM design. A Manufacturing Model is a derive of the Design scene, which can be augmented without a |
| `ManufacturingModelInput` | core.Base | This class defines the methods and properties that pertain to the definition of a ManufacturingModel. |
| `ManufacturingModels` | core.Base | Referenced from CAM product to access manufacturing models in document. |
| `ModifyUtility` | core.Base | Base class for all modify utilities. |
| `MultiAxisFeedrateSettings` | core.Base | Base class for the multi-axis feedrate settings |
| `MultiAxisFeedrateSettingsInput` | core.Base | Input class for creating MultiAxisFeedrateSettings objects. |
| `MultiAxisRetractAndReconfigureSettings` | core.Base | Settings for multi-axis retract and reconfigure. |
| `MultiAxisSingularityLinearizationSettings` | core.Base | The class for the multi-axis singularity linearization settings. |
| `MultiAxisSingularitySettings` | core.Base | Base class for multi-axis singularity settings. |
| `NCProgramInput` | core.Base | The NCProgramInput holds all necessary information to create a new NC program. |
| `NCProgramPostProcessOptions` | core.Base | The NCProgramPostProcessOptions provides settings to control the post processing of NC programs. |
| `NCPrograms` | core.Base | Container for all NC programs. Referenced from CAM product to access NC programs in a document, similar to what Setups is for all setup obje |
| `OperationBase` | core.Base | Base class object representing all operations, folders, patterns and setups. |
| `OperationInput` | core.Base | The OperationInput holds all necessary informations to create a new Operation. |
| `Operations` | core.Base | Collection that provides access to the individual operations within an existing setup, folder or pattern. |
| `OperationStrategy` | core.Base | The OperationStrategy contains information about a strategy such as its name, title and description. |
| `OptimizedOrientationResult` | core.Base | The orientation result instance. |
| `ParameterValue` | core.Base | Base class for representing the value of a parameter. |
| `PostConfiguration` | core.Base | Object that represents a post configuration. |
| `PostConfigurationQuery` | core.Base | A PostConfigurationQuery can be used to search a LibraryLocation for a set of PostConfiguration objects matching the required properties. |
| `PrintSetting` | core.Base | Object that represents a PrintSetting. |
| `PrintSettingItem` | core.Base | Collection that provides access to the print setting parameters. |
| `PrintSettingQuery` | core.Base | A PrintSettingQuery can be used to search a LibraryLocation for a set of PrintSetting objects matching the required properties. |
| `RecognizedHole` | core.Base | Object that represents a hole, a hole is made of one or more segments. |
| `RecognizedHoleGroup` | core.Base | Object that represents a collection of holes that contain similar geometry. Holes have similar geometry if they contain the same segment typ |
| `RecognizedHoleGroups` | core.Base | Object that represents a collection of hole groups. |
| `RecognizedHoles` | core.Base | Object that represents a collection of holes. |
| `RecognizedHoleSegment` | core.Base | Object that represents a hole segment, i.e. a single geometric shape like a cylinder or cone within the context of a hole. |
| `RecognizedHolesInput` | core.Base | Object that contains the settings used by recognizedHoles and recognizedHoleGroups. |
| `RecognizedPocket` | core.Base | Object that represents a single pocket (an outer boundary with depth and optional islands) |
| `RecognizedPocketInput` | core.Base | Input object containing properties used to recognize pockets. Includes bosses along open and closed pockets. |
| `RecognizedPockets` | core.Base | Object that represents a collection of pockets. |
| `ScratchPolygonSelection` | core.Base | Represents a single scratch polygon selection - a user-drawn polygon defined by a series of 3D points. |
| `ScratchPolygonSelections` | core.Base | Collection for all scratch polygon selections to be passed to a CadScratchPolygonsParameterValue |
| `SetupChangeEventHandler` | core.EventHandler | The SetupChangeEventHandler is a client implemented class that can be added as a handler to a |
| `SetupEventHandler` | core.EventHandler | The SetupEventHandler is a client implemented class that can be added as a handler to a |
| `SetupInput` | core.Base | Object that represents setup creation parameters. |
| `Setups` | core.Base | Collection that provides access to all of the existing setups in a document. |
| `SetupVisibilityManager` | core.Base | Class to manage the visibility of various elements of the setup. |
| `StockMaterial` | core.Base | Represents a StockMaterial. |
| `Tool` | core.Base | Represents a Tool. |
| `ToolLibrary` | core.Base | ToolLibrary represents a collection of Tool objects. |
| `ToolPreset` | core.Base | A Preset defines the material specific properties of a Tool. |
| `ToolPresets` | core.Base | ToolPresets represents a collection of ToolPreset. |
| `ToolQuery` | core.Base | ToolQuery objects are used to search for a set of Tools or ToolLibrary objects inside of the ToolLibraries collection or for a set of Tools  |
| `ToolQueryResult` | core.Base | The ToolQueryResult represents one result item of a ToolQuery. |
| `AdditiveFEAOperation` | OperationBase | The AdditiveFEAOperation represents a finite element analysis for |
| `AdditiveFEAOperationInput` | OperationInput |  |
| `AdditiveFEAUtility` | ModifyUtility | AdditiveFEAUtility provides functionality for additive FEA simulation operations. |
| `AdditiveFFFLimitsMachineElement` | MachineElement | Machine element representing limits for fused filament fabrication (FFF) machine motion and temperatures. |
| `AdditiveInterferenceAnalysisResult` | GeneratedData | Result of an additive interference analysis operation. |
| `AdditivePlatformMachineElement` | MachineElement | Machine element representing the additive platform settings. |
| `AdditiveSetupUtility` | ModifyUtility | AdditiveSetupUtility provides functionality for modifications of additive setups. |
| `ArrangeSelection` | GeometrySelection | Class for arrange selections. Provides access to the selected geometry and its properties. |
| `BooleanParameterValue` | ParameterValue | A parameter value that is a boolean. |
| `CadContours2dParameterValue` | ParameterValue | A parameter value that is a CadContours2dParameterValue. |
| `CadMachineAvoidGroupsParameterValue` | ParameterValue | A parameter value that is a CadMachineAvoidGroupsParameterValue. |
| `CadObjectParameterValue` | ParameterValue | A parameter value that is a collection of cad objects. |
| `CadScratchPolygonsParameterValue` | ParameterValue | A parameter value for toolpath edit operations that use scratch polygon geometry, |
| `CAM` | core.Product | Object that represents the CAM environment of a Fusion document. |
| `CAM3MFExportOptions` | CAMExportOptions | 3MF export option. Available with all additive machines except Formlabs. Expects a setup as its export object. |
| `CAMAdditiveBuildExportOptions` | CAMExportOptions | Additive buildfile export option. Available with all additive machines except for FFF and DED based machines. |
| `CAMAdditiveContainer` | OperationBase | Object that represents an additive container in an existing Setup. |
| `CAMArrangeParameterValue` | ParameterValue | A parameter value that is a CAMArrangeParameterValue. |
| `CAMFolder` | OperationBase | Object that represents a folder in an existing Setup, Folder or Pattern. |
| `CAMHoleRecognition` | OperationBase | Object that represents a hole recognition object in an existing Setup, Folder or Pattern. |
| `CAMTemplateLibrary` | CAMLibrary | The CAMTemplateLibrary provides access to templates. Using this object you can import templates |
| `ChoiceParameterValue` | ParameterValue | A parameter value that is a list of choices. |
| `ControllerConfigurationMachineElement` | MachineElement | Machine element representing controller settings for kinematics. |
| `CurveSelection` | GeometrySelection | Base class of all curve based geometry selections. |
| `DocumentToolLibrary` | ToolLibrary | DocumentToolLibrary provides access to tools used by the document. It supports |
| `ExtruderMachineElement` | MachineElement | Machine element representing an extruder on a fused filament fabrication (FFF) machine. |
| `ExtruderMachineElementInput` | MachineElementInput | Specialization of MachineElementInput for creating an additive FFF extruder element. |
| `FloatParameterValue` | ParameterValue | A parameter value that is a floating point value. |
| `IntegerParameterValue` | ParameterValue | A parameter value that is an integer. |
| `InteractionsMachineElement` | MachineElement | Machine element representing the machine's interactions. |
| `KinematicsMachineElement` | MachineElement | Machine element representing the machine's kinematics tree. |
| `LinearMachineAxis` | MachineAxis | Object that represents an axis with linear motion (e.g. X, Y, and Z). |
| `LinearMachineAxisConfiguration` | MachineAxisConfiguration | A MachineAxisConfiguration holding settings specific to linear axes. |
| `LinearMachineAxisInput` | MachineAxisInput | Object that defines the properties required to create a new linear machine axis object. |
| `MachineAvoidSelectionBase` | GeometrySelection | Base parent class for all machine/avoid selection classes. |
| `MachineFromFileInput` | MachineInput | Object used as input to create a machine from a local file. |
| `MachineFromLibraryInput` | MachineInput | Object used as input to create a machine from library URL. |
| `MachineFromTemplateInput` | MachineInput | Object used as input to create a machine from a given template. |
| `MachineLibrary` | CAMLibrary | The MachineLibrary provides access to machines. Using this object you can import machines |
| `MultiAxisDPMFeedrateSettings` | MultiAxisFeedrateSettings | Specialization of MultiAxisFeedrateSettings for standard degrees per minute feedrates. |
| `MultiAxisInverseTimeFeedrateSettings` | MultiAxisFeedrateSettings | Specialization of MultiAxisFeedrateSettings for inverse time feedrates. |
| `MultiAxisMachineElement` | MachineElement | Machine element representing multi-axis machine settings. |
| `MultiAxisMachineElementInput` | MachineElementInput | Specialization of MachineElementInput for creating a multi-axis machine element. |
| `MultiAxisProgrammedFeedrateSettings` | MultiAxisFeedrateSettings | Specialization of MultiAxisFeedrateSettings for programmed feedrates. |
| `NCProgram` | OperationBase | Object that represents an existing NC program. |
| `Operation` | OperationBase | Object that represents an operation in an existing Setup, Folder or Pattern. |
| `OptimizedOrientationResults` | GeneratedData | Collection of OptimizedOrientationResult instances associated with a given optimized orientation object inside an additive setup. |
| `PostLibrary` | CAMLibrary | The PostLibrary provides access to post configurations. Using this object you can import post configurations |
| `PostProcessingMachineElement` | MachineElement | Machine element representing the post processor and post properties. |
| `PrintSettingLibrary` | CAMLibrary | The PrintSettingLibrary provides access to PrintSettings. Using this object you can import PrintSettings |
| `PRMExportOptions` | CAMExportOptions | PRM export options for additive FEA.  A PRM file can only be |
| `RotaryMachineAxis` | MachineAxis | Object that represents an axis with rotary motion (e.g. A, B, and C). |
| `RotaryMachineAxisConfiguration` | MachineAxisConfiguration | A MachineAxisConfiguration holding settings specific to rotary axes. |
| `RotaryMachineAxisInput` | MachineAxisInput | Object that defines the properties required to create a new rotary machine axis object. |
| `Setup` | OperationBase | Object that represents an existing Setup. |
| `SetupChangeEvent` | core.Event | A SetupChangeEvent represents a setup related change event.  It is used for SetupChanged notifications. |
| `SetupChangeEventArgs` | core.EventArgs | The SetupChangeEventArgs provides information associated with a change event of a setup. |
| `SetupEvent` | core.Event | A SetupEvent represents a setup related event.  For example, SetupCreated or SetupDestroying. |
| `SetupEventArgs` | core.EventArgs | The SetupEventArgs provides information associated with a setup event. |
| `StockMaterialLibrary` | CAMLibrary | The StockMaterialLibraries object provides utilities to access, import and update stock material by URL. |
| `StringParameterValue` | ParameterValue | A parameter value that is a string. |
| `ToolBlock` | Tool | Represents a Tool Block. |
| `ToolingCapabilitiesMachineElement` | MachineElement | Machine element representing the tooling capabilities of a machine. |
| `ToolingCapabilitiesMachineElementInput` | MachineElementInput | Input class for creating ToolingCapabilitiesMachineElement objects. |
| `ToolLibraries` | CAMLibrary | The ToolLibraries object provides utilities to access, import and update tool libraries. |
| `TurningTool` | Tool | Represents a Turning Tool. |
| `CAMPattern` | CAMFolder | Object that represents a pattern in an existing Setup, Folder or Pattern. |
| `ChainSelection` | CurveSelection | Represents a chain type of curve selection. Allows B-Rep edges and sketch geometry for the inputGeometry property. |
| `FaceContourSelection` | CurveSelection | Represents a face type of curve selection. It allows BRepFace objects for the input geometry. |
| `MachineAvoidDefaultSelection` | MachineAvoidSelectionBase | Machine/avoid default selection class. Represents a group of selections that are parameter |
| `MachineAvoidDirectSelection` | MachineAvoidSelectionBase | Machine/avoid direct selection class. Represents a group of direct selections that |
| `MultiAxisCombinationDPMFeedrateSettings` | MultiAxisDPMFeedrateSettings | Specialization of MultiAxisDPMFeedrateSettings for degrees per minute feedrates that require a combination of linear and rotary movements. |
| `PocketRecognitionSelection` | CurveSelection | Pocket type curve selection. It searches for pockets matching the criteria on the selected bodies |
| `PocketSelection` | CurveSelection | Pocket type for a curve selection. Allows planar BREP face selections for the input geometry. |
| `SilhouetteSelection` | CurveSelection | Represents a silhouette type of curve selection. Allows BRepBody selections for the input geometry. |
| `SketchSelection` | CurveSelection | Represents a sketch curve selection. It allows entire sketches for the input geometry. |
