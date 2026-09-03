# Class index: adsk.sim

64 classes/enums found in `references/api-stubs/sim.py`. Use `grep -n "^class ClassName" references/api-stubs/sim.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `ConstraintTypes` |  | Simulation constraint types. |
| `ContactTypes` |  | Contact types |
| `ElementOrderTypes` |  | Mesh element order types. |
| `ElementSizeDeterminationTypes` |  | Determination of the average element size. |
| `ForceUnits` |  | Valid force unit types for simulation studies. |
| `LoadTypes` |  | Load types. |
| `PrecheckMessageSeverities` |  | Severity level of a pre-check message. |
| `PrecheckStates` |  | Pre-check state indicating whether the study is ready to solve. |
| `SafetyFactorTypes` |  | Material safety factor types. |
| `SimulationUnitSystems` |  | Predefined unit systems available for simulation studies. |
| `StudyResultStates` |  | The state of the study's solve results. |
| `StudyTypes` |  | Simulation study types. |
| `VectorDefinitionTypes` |  | Load vector definition types. |
| `AngularAccelerationDefinition` | core.Base | Object that represents an angular acceleration definition. |
| `Constraint` | core.Base | Object that represents a constraint. |
| `ConstraintMaskDefinition` | core.Base | Object that represents a structural constraint mask. |
| `Constraints` | core.Base | Provides access to a collection of constraints in a load case. |
| `ContactBase` | core.Base | Base class for contacts. |
| `ContactInput` | core.Base | This class defines the methods and properties that pertain to the definition of a contact. |
| `Contacts` | core.Base | Provides access to contacts in a study. |
| `GeneralSettings` | core.Base | Object that represents simulation general settings. |
| `Load` | core.Base | Object that represents a load. |
| `LoadCase` | core.Base | Object that represents a LoadCase inside a study. |
| `LoadCases` | core.Base | Provides access to the LoadCases in the study. |
| `LoadInput` | core.Base | Base input object used when creating a load object. |
| `Loads` | core.Base | Provides access to a collection of loads in a load case. |
| `MeshSettings` | core.Base | Object that represents simulation mesh settings. |
| `OptionalDouble` | core.Base | Represents an optional double value. |
| `PrecheckMessage` | core.Base | Represents a single pre-check validation message (error or warning). |
| `Settings` | core.Base | Object that represents all simulation settings. |
| `SimDefaultUnits` | core.Base | Controls the default display units for simulation quantities such as force, |
| `SimulationModel` | core.Base | Object that represents a simulation model inside the simulation workspace. |
| `SimulationModels` | core.Base | Provides access to the simulation models in the simulations object. |
| `SolveSettings` | core.Base | Object that represents simulation solve settings. |
| `StructuralConstraintInput` | core.Base | This class defines the methods and properties that pertain to the definition of a structural constraint. |
| `Studies` | core.Base | Provides access to the Studies in the simulation model. |
| `Study` | core.Base | Object that represents a study inside a simulation model. |
| `StudyMaterial` | core.Base | Provides access to the study material. |
| `TransientDefinition` | core.Base | Object that represents a transient definition. |
| `VectorDefinition` | core.Base | Object that represents a vector definition. |
| `AngularAccelerationLoadInput` | LoadInput | Input object for creating an angular global (angular acceleration) load. |
| `AngularGlobalLoad` | Load | Object that represents an angular global load. |
| `BearingLoad` | Load | Object that represents a bearing load. |
| `Contact` | ContactBase | Contact class with methods for reading and modifying contact properties |
| `CoolingLoadInput` | LoadInput | Input object for creating a directional cooling load (fan attribute, heat sink). |
| `FanAttributeLoad` | Load | Object that represents a fan attribute load. |
| `ForceLoad` | Load | Object that represents a force load. |
| `GravityLoad` | Load | Object that represents a gravity load. |
| `HeatSinkLoad` | Load | Object that represents a heat sink load. |
| `HydrostaticPressureLoad` | Load | Object that represents a hydrostatic pressure load. |
| `LinearGlobalLoad` | Load | Object that represents a linear global load. |
| `MomentLoad` | Load | Object that represents a moment load. |
| `PressureLoad` | Load | Object that represents a pressure load. |
| `RadiationLoad` | Load | Object that represents a thermal radiation load. |
| `Simulations` | core.Product | Object that represents the simulations environment of a Fusion document. |
| `SimUnitsManager` | core.UnitsManager | Extends the base UnitsManager with helpers for converting simulation-specific |
| `SolveFuture` | core.Future | Represents the asynchronous result of a solve operation. |
| `StructuralConstraint` | Constraint | Object that represents a structural constraint. |
| `StructuralLoadInput` | LoadInput | Input object for creating a structural load (pressure, force, moment, bearing, gravity, linear global). |
| `TemperatureLoad` | Load | Object that represents an applied temperature load. |
| `ThermalConvectionLoad` | Load | Object that represents a thermal convection load. |
| `ThermalInternalHeatLoad` | Load | Object that represents a thermal internal heat load. |
| `ThermalLoadInput` | LoadInput | Input object for creating thermal loads (applied temperature, thermal convection, thermal radiation, thermal internal heat, thermal surface  |
| `ThermalSurfaceHeatLoad` | Load | Object that represents a thermal surface heat (heat source) load. |
