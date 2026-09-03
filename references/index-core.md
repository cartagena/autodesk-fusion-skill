# Class index: adsk.core

343 classes/enums found in `references/api-stubs/core.py`. Use `grep -n "^class ClassName" references/api-stubs/core.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `AppearanceSourceTypes` |  | The different types of sources for an appearance. |
| `AppearanceSurfaceTypes` |  | The kind of surface a new Appearance represents when created via |
| `BooleanOptions` |  | The different values that can be used when specifying whether an item |
| `CameraTypes` |  | The different types of cameras. |
| `CloseError` |  | List of possible errors when closing a document. |
| `CommandTerminationReason` |  | Defines the termination reason for a command. |
| `Curve2DTypes` |  | The different types of 2D curves. |
| `Curve3DTypes` |  | The different types of 3D curves. |
| `DefaultModelingOrientations` |  | A list of the valid modeling orientations. |
| `DefaultOrbits` |  | A list of the valid orbit modes. |
| `DegradedSelectionDisplayStyles` |  | A list of the valid degraded display styles. |
| `DegreeDisplayFormats` |  | List of the valid degree display formats. |
| `DialogResults` |  | Defines the valid return types from a dialog. |
| `DocumentTypes` |  | The types of documents that can be created. |
| `DropDownStyles` |  | Defines the different styles that a drop-down input can be. |
| `FootAndInchDisplayFormats` |  | List of the valid foot and inch formats. |
| `FutureStates` |  | The different states of a future. |
| `GenericErrors` |  | Errors that every API call can return via Application::GetLastError. |
| `GraphicsDrivers` |  | A list of the graphics driver that are supported for various settings in Fusion. |
| `GraphicsPresets` |  | Defines the different options for preset graphic setting definitions. |
| `HorizontalAlignments` |  | Defines the different horizontal alignments that can be applied to text. |
| `HttpMethods` |  | The HTTP methods supported by the HttpRequest object. |
| `HubTypes` |  | The different types of hubs. |
| `JobStatus` |  | Status of an asynchronous Fusion job. |
| `KeyboardModifiers` |  | Keyboard modifier values. |
| `KeyCodes` |  | Key values on the keyboard. |
| `LightingEnvironments` |  | Defines the list of available lighting environments. |
| `ListControlDisplayTypes` |  | The different types of items that can be displayed in a list control. |
| `LogLevels` |  | Log message level |
| `LogTypes` |  | Location where messages should be logged. |
| `MaterialDisplayUnits` |  | List of the different types of material related units supported for displaying values. |
| `MessageBoxButtonTypes` |  | Defines the valid return types from a message box. |
| `MessageBoxIconTypes` |  | Defines the different icons that can be used in a message box. |
| `MouseButtons` |  | Mouse button values. |
| `NetworkProxySettings` |  | A list of the valid network proxy settings. |
| `NurbsSurfaceProperties` |  | The different surface property types. |
| `OpenDocumentError` |  | The possible errors when a document is opened. |
| `OperatingSystems` |  | Defines the various operating systems that a script or add-in can run on. |
| `PaletteDockingOptions` |  | Defines the different options available when docking a palette to the Fusion main window area. |
| `PaletteDockingStates` |  | Defines the docking states that a palette can be in, such as floating, or docked to the top, bottom, left, or right of the main window. |
| `PaletteSnapOptions` |  | Defines the positions that a palette can be snapped to another palette, such as top, left, or right. |
| `PanZoomOrbitShortcuts` |  | A list of the different predefined keyboard shortcuts for pan, zoom, and orbit. |
| `ProgrammingLanguages` |  | Defines the various languages supported for Fusion scripts and add-ins. |
| `ProjectedTextureMapTypes` |  | The different types of projected texture maps. |
| `SaveLocalErrors` |  | List of possible errors when saving a document locally. |
| `ScriptSourceLocations` |  | Defines the different locations where Fusion looks for scripts and add-ins. |
| `SelectionDisplayStyles` |  | A list of the valid selection display styles. |
| `StatusMessageTypes` |  | The different types of status messages that can be used with the StatusCode object. |
| `SurfaceTypes` |  | The different types of surfaces. |
| `TablePresentationStyles` |  | The different styles that a TableCommandInput can use for its display. |
| `TextureTypes` |  | The different types of textures. |
| `TransparencyDisplayEffects` |  | A list of the valid transparency display effects. |
| `TriadChanges` |  | Defines the different types of edits that can be applied by the user to a triad command input. |
| `UploadStates` |  | The different states of a file upload process. |
| `UserInterfaceThemes` |  | Defines the different color themes used by the user interface. |
| `UserLanguages` |  | A list of the valid languages. |
| `ValueInputError` |  | Errors that can occur when using the ValueInput object. |
| `ValueTypes` |  | The different types of values that a ValueInput can be. |
| `VectorError` |  | Error values for various vector operations. |
| `VerticalAlignments` |  | Defines the different vertical alignments that can be applied to text. |
| `ViewOrientations` |  | Common view orientations. |
| `VisualStyles` |  | A list of the support visual styles that Fusion uses when rendering the model. |
| `Base` |  | The base class that all other classes are derived from. |
| `EventHandler` |  | A client supplies an EventHandler and adds it to one or more Events in |
| `ActiveSelectionEventHandler` | EventHandler | The ActiveSelectionEventHandler is a client implemented class that can be added as a handler to a |
| `APIPreferences` | Base | Provides access to the various preferences associated with the API. |
| `Appearance` | Base | An appearance. |
| `Appearances` | Base | A collection of appearances. |
| `AppearanceTexture` | Base | Provides access to a list of properties that define a texture. |
| `Application` | Base | The top-level object that represents the Fusion application (all of Fusion). |
| `ApplicationCommandEventHandler` | EventHandler | An application command event handler base class that a client derives from to handle events triggered by an |
| `ApplicationEventHandler` | EventHandler | The ApplicationEventHandler is a client implemented class that can be added as a handler to an |
| `ApplicationFolders` | Base | The ApplicationFolders object provides access to the paths of folders associated with Fusion, |
| `Attribute` | Base | Represents an attribute associated with a specific entity, Product, or Document. |
| `Attributes` | Base | Provides access to attributes associated with a specific entity, |
| `BoundingBox2D` | Base | Transient object that represents a 2D bounding box. A 2D bounding box is a rectangle box that is parallel |
| `BoundingBox3D` | Base | Transient object that represents a 3D bounding box. |
| `Camera` | Base | The Camera class represents the information that specifies how a model is |
| `CameraEventHandler` | EventHandler | The CameraEventHandler is a client implemented class that can be added as a handler to an |
| `CanvasEffects` | Base | Provides access to the settings that control the canvas effects. |
| `CloudFileDialog` | Base | Provides access to a cloud file dialog. A cloud file dialog can be used to prompt the user |
| `CloudFolderDialog` | Base | Represents a cloud folder dialog, which is a dialog that is used to prompt the user |
| `Color` | Base | The Color class wraps all of the information that defines a simple color. |
| `Command` | Base | The Command class contains all of the functionality needed by a command to gather |
| `CommandCreatedEventHandler` | EventHandler | Class that contains the call back function that is called when the CommandCreated event is fired. |
| `CommandDefinition` | Base | The CommandDefinition is the base class of command types such as ButtonDefinition, CheckBoxDefinition, and DropDownCommandDefinition. Comman |
| `CommandDefinitions` | Base | Provides access to all of the available command definitions. This is all those created via |
| `CommandEventHandler` | EventHandler | An command event handler base class that a client derives from to handle events triggered by a CommandEvent. |
| `CommandInput` | Base | The base class for all command inputs. A CommandInput is used to gather an input value from the user when a command is executed. |
| `CommandInputs` | Base | Provides access to the set of inputs for a command. Command inputs are used to gather inputs from the user when a command is executed. |
| `CompatibilityPreferences` | Base | The CompatibilityPreferences object provides access to compatibility and troubleshooting |
| `ControlDefinition` | Base | The ControlDefinition is the base class for control definition types such as ButtonDefinition, CheckBoxDefinition, and DropDownCommandDefini |
| `CopyFileInput` | Base | The base class for any copy file input objects. |
| `Curve2D` | Base | The base class for all 2D transient geometry classes. |
| `Curve3D` | Base | The base class for all 3D transient geometry classes. |
| `Curve3DPath` | Base | Object that represents a collection of connected Curve3D objects. |
| `CurveEvaluator2D` | Base | 2D curve evaluator that is obtained from a transient curve and allows you to perform |
| `CurveEvaluator3D` | Base | 3D curve evaluator that is obtained from a transient curve and allows you to perform |
| `CustomEventHandler` | EventHandler | The ApplicationEventHandler is a client implemented class that can be added as a handler to an |
| `Data` | Base | The Data class provides access to data files |
| `DataComponent` | Base | An object that provides ID's that can be used to access the component using MFG DM API. |
| `DataEventHandler` | EventHandler | The DataEventHandler is a client implemented class that can be added as a handler to a |
| `DataFile` | Base | A data file in a data folder. |
| `DataFileFuture` | Base | Used to check the state and get back the results of a file upload. |
| `DataFiles` | Base | Returns the items within a folder. This includes everything in a folder except for other folders. |
| `DataFolder` | Base | A data folder that contains a collection of data items. |
| `DataFolders` | Base | Collection object that provides a list of data folders. |
| `DataHub` | Base | Represents a hub within the data. |
| `DataHubs` | Base | Collection object that provides a list of all available hubs. |
| `DataObject` | Base | The DataObject provides access to the raw data that represents a logical entity. Typically, |
| `DataProject` | Base | Represents the master branch project within a hub. |
| `DataProjects` | Base | Collection object that provides a list of all available projects. |
| `DefaultUnitsPreferences` | Base | The base class for the default units preference. There is a derived class |
| `DefaultUnitsPreferencesCollection` | Base | A collection that provides access to product specific unit preference objects. |
| `Document` | Base | Object that represents an open document. This is the base class for all document types. |
| `DocumentEventHandler` | EventHandler | The DocumentEventHandler is a client implemented class that can be added as a handler to a |
| `DocumentReference` | Base | Represents a reference to a document from another document. |
| `DocumentReferences` | Base | Provides access to the list of documents referenced from a document. |
| `Documents` | Base | The Documents object provides access to all of the currently open documents and |
| `Event` | Base | Objects can have several Event properties that fire when |
| `EventArgs` | Base | When an event handler is called, it is passed |
| `FavoriteAppearances` | Base | Collection of the favorite appearances. |
| `FavoriteMaterials` | Base | Collection of the favorite materials. |
| `FileDialog` | Base | Provides access to a file dialog. A file dialog can be used to prompt the user |
| `FileOpenContext` | Base | An object that represents context information for opening a file. |
| `FolderDialog` | Base | Provides access to a folder selection dialog to allow the user to select a folder. |
| `Future` | Base | The base class for futures. |
| `GeneralPreferences` | Base | Provides access to the general preferences. |
| `GraphicsPreferences` | Base | The GraphicsPreferences object provides access to the various graphics related preferences. |
| `GridPreferences` | Base | The GridPreferences object provides access to grid related preferences. |
| `HTMLEventHandler` | EventHandler | The HTMLEventHandler is a client implemented class that can be added as a handler to a HTML |
| `HttpEventHandler` | EventHandler | The HttpEventHandler is a client implemented class that can be added as a handler to an |
| `HttpRequest` | Base | Supports the ability to make HTTP requests. |
| `HttpResponse` | Base | An object that provides the data associated with an HTTP response. |
| `ImportManager` | Base | Provides access to functionality to support importing various modeling formats into Fusion. |
| `ImportOptions` | Base | The base class for the different import types. This class is never directly used |
| `InputChangedEventHandler` | EventHandler | An event handler base class that a client derives from to handle events triggered by a InputChangedEvent. |
| `Job` | Base | Base class for all Jobs. |
| `KeyboardEventHandler` | EventHandler | An event handler base class that a client derives from to handle events triggered by a KeyboardEvent. |
| `LinearMarkingMenu` | Base | Represents the linear marking menu which is the vertical menu that's displayed when the user right-clicks |
| `ListItem` | Base | Represents a single item in a check box list or a drop-down command input. |
| `ListItems` | Base | Provides access to the list of items in a check box list. This object supports the ability to add |
| `MarkingMenuEventHandler` | EventHandler | The MarkingMenuEventHandler is a client implemented class that can be added as a handler to a |
| `Material` | Base | A material. |
| `MaterialLibraries` | Base | The MaterialLibraries collection object provides access to |
| `MaterialLibrary` | Base | A material library. |
| `MaterialPreferences` | Base | Provides access to the material related preferences. |
| `Materials` | Base | Collection of materials within a Library or Design. |
| `Matrix2D` | Base | Transient 2D 3x3 matrix. This object is a wrapper over 2D matrix data and is used as way to pass matrix data |
| `Matrix3D` | Base | Transient 3D 4x4 matrix. This object is a wrapper over 3D matrix data and is used as way to pass matrix data |
| `MeasureManager` | Base | The MeasurementManager class provides some generic measurement utilities that |
| `MeasureResults` | Base | Provides measurement results from the various measurement methods available on the MeasureManager object. |
| `MFGDMDataEventHandler` | EventHandler | The MFGDMDataEventHandler is a client implemented class that can be added as a handler to a MFGDMDataEvent. |
| `Milestone` | Base | An object that represents a milestone. |
| `Milestones` | Base | Returns the milestones associated with a DataFile. |
| `MouseEventHandler` | EventHandler | An event handler base class that a client derives from to handle events triggered by a MouseEvent. |
| `NamedValues` | Base | Wraps a list of named values. |
| `NamedView` | Base | Represents a named view as seen in the browser. |
| `NamedViews` | Base | Collection that provides access to all of the existing named views associated |
| `NavigationEventHandler` | EventHandler | The NavigationEventHandler is a client implemented class that can be added as a handler to a Navigation |
| `NetworkPreferences` | Base | The NetworkPreferences object provides access to network related preferences. |
| `ObjectCollection` | Base | Generic collection used to handle lists of any object type. |
| `OrientedBoundingBox3D` | Base | Transient object that represents an oriented 3D bounding box. An oriented 3D bounding box is a rectangular box that |
| `Palette` | Base | A Palette is a floating or docked dialog in Fusion. The browser is an |
| `Palettes` | Base | Provides access to a set of palettes, which are docked or floating windows that display HTML. |
| `PersonalUseLimits` | Base | Object that provides information about file limits associated with a "Fusion for Personal Use license". |
| `Point2D` | Base | Transient 2D point. A transient point is not displayed or saved in a document. |
| `Point3D` | Base | Transient 3D point. A transient point is not displayed or saved in a document. |
| `Preferences` | Base | The Preferences object provides access to the various preference related objects |
| `Product` | Base | The base class for the various product specific containers. For |
| `ProductPreferences` | Base | The base class for the general product preferences. There is a derived class |
| `ProductPreferencesCollection` | Base | A collection that provides access to product specific preference objects. |
| `Products` | Base | The Products object provides access to all of the products that exist in the document. |
| `ProductUsageData` | Base | Provides access to the product usage data settings. |
| `ProgressBar` | Base | Provides access to the progress bar. |
| `ProgressDialog` | Base | Provides access to the progress dialog. |
| `Properties` | Base | A collection of properties that are associated with a material or appearance. |
| `Property` | Base | The base class for the specific property types used by materials and appearances. |
| `PropertyGroup` | Base | Represents a group of properties and provides access to the properties. |
| `PropertyGroups` | Base | A collection of PropertyGroup objects. |
| `RadialMarkingMenu` | Base | Represents the marking menu which is the round menu that's displayed when the user right-clicks |
| `SaveImageFileOptions` | Base | Class that defines the various options that can be used when saving a viewport as an image. This |
| `Script` | Base | Object that represents a script or add-in. |
| `ScriptInput` | Base | Used when creating a new script or add-in to specify all of the required |
| `Scripts` | Base | API object that provides equivalent functionality of the "Scripts and Add-Ins" dialog. |
| `Selection` | Base | Provides access to a selection of an entity in the user interface. |
| `SelectionEventHandler` | EventHandler | An event handler base class that a client derives from to handle events triggered by a SelectionEvent. |
| `SelectionFilters` | Base | Provides access to the various filter settings for selections. |
| `SelectionFilterSettings` | Base | Provides management of selection filters. Supports registration of |
| `Selections` | Base | Provides access to and control over the set of selected entities in the user interface. |
| `SelectionSet` | Base | The SelectionSet object represents a Selection Set as seen in the user interface. Using a SelectionSet, |
| `SelectionSets` | Base | The SelectionSets object is used to create and access existing selection sets. |
| `SharedLink` | Base | Provides access to the URL that can be used to share this DataFile with others. This object |
| `Status` | Base | Used to communicate the current status of an object or operation. This provides the status |
| `StatusMessage` | Base | Defines the message associated with a Status object. |
| `StatusMessages` | Base | A collection of status messages associated with a Status object. The primary purpose of the messages is to |
| `Surface` | Base | Describes a two-dimensional topological, manifold in three-dimensional space. |
| `SurfaceEvaluator` | Base | Surface evaluator that is obtained from a transient surface and allows you to perform |
| `TextureMapControl` | Base | Provides access to the settings that control how a texture is applied to a body or mesh, |
| `Toolbar` | Base | Provides access to a toolbar in the user interface. A toolbar is a collection of toolbar controls. |
| `ToolbarControl` | Base | The base class for all toolbar controls. |
| `ToolbarControlList` | Base | Provides access to a list of toolbar controls. |
| `ToolbarControls` | Base | ToolbarControls is a collection of ToolbarControl objects displayed in a toolbar or menu. |
| `ToolbarPanel` | Base | Toolbar panels are the panels shown in the command toolbar. |
| `ToolbarPanelList` | Base | A ToolbarPanelList is a list of ToolbarPanel objects. |
| `ToolbarPanels` | Base | Provides access to a set of toolbar panels. Many toolbar panels exist and their |
| `Toolbars` | Base | Provides access to the toolbars. These are currently the right and left QAT's and the NavBar. |
| `ToolbarTab` | Base | Toolbar tabs are the tabs shown in the command toolbar. |
| `ToolbarTabList` | Base | A ToolbarTabList is a list of ToolbarTab objects. |
| `ToolbarTabs` | Base | Provides access to a set of toolbar tabs. |
| `UnitAndValuePreferences` | Base | The UnitAndValuePreferences object provides access to unit and value precision |
| `UnitsManager` | Base | Utility class used to work with Values and control default units. |
| `URL` | Base | A URL object provides useful and easy-to-use methods for creating, modifying, and analyzing URLs. |
| `User` | Base | A class that represents a Fusion User |
| `UserInterface` | Base | Provides access to the user-interface related objects and functionality. |
| `UserInterfaceGeneralEventHandler` | EventHandler | The UserInterfaceGeneralEventHandler is a client implemented class that can be |
| `ValidateInputsEventHandler` | EventHandler | An event handler base class that a client derives from to handle events triggered by a ValidateInputsEvent. |
| `ValueInput` | Base | A ValueInput provides a flexible way of specifying a string, a double, a boolean, or object reference. |
| `Vector2D` | Base | Transient 2D vector. This object is a wrapper for 2D vector data and is used to |
| `Vector3D` | Base | Transient 3D vector. This object is a wrapper over 3D vector data and is used as way to pass vector data |
| `Viewport` | Base | A viewport within Fusion. A viewport is the window where the model is displayed. |
| `WebRequestEventHandler` | EventHandler | The WebRequestEventHandler is a client implemented class that can be added as a handler to an |
| `Workspace` | Base | A Workspace provides access to a set of panels, which contain commands that |
| `WorkspaceEventHandler` | EventHandler | The WorkspaceEventHandler is a client implemented class that can be added as a handler to a |
| `WorkspaceList` | Base | A WorkspaceList is a list of Workspaces - e.g. the Workspaces for a given product. |
| `Workspaces` | Base | Provides access to all of the existing workspaces. |
| `ActiveSelectionEvent` | Event | This event fires whenever the contents of the active selection changes. This occurs as the user |
| `ActiveSelectionEventArgs` | EventArgs | The ActiveSelectionEventArgs provides information associated with the active selection changing. |
| `AngleValueCommandInput` | CommandInput | Represents a command input that gets an angle from the user. This displays |
| `AppearanceTextureProperty` | Property | A texture value property associated with a material or appearance. |
| `ApplicationCommandEvent` | Event | An event endpoint that supports the connection to ApplicationCommandEventHandlers. |
| `ApplicationCommandEventArgs` | EventArgs | Provides a set of arguments from a firing ApplicationCommandEvent to an ApplicationCommandEventHandler's |
| `ApplicationEvent` | Event | An ApplicationEvent represents a Fusion application related event. For example, startupCompleted or OnlineStatusChanged |
| `ApplicationEventArgs` | EventArgs | The ApplicationEventArgs provides information associated with an application event. |
| `Arc2D` | Curve2D | Transient 2D arc. A transient arc is not displayed or saved in a document. |
| `Arc3D` | Curve3D | Transient 3D arc. A transient arc is not displayed or saved in a document. |
| `BooleanProperty` | Property | A property that is a Boolean value. |
| `BoolValueCommandInput` | CommandInput | Provides a command input to get a boolean value from the user. This is represented |
| `BrowserCommandInput` | CommandInput | Browser command inputs behave as a browser where you can define HTML to be displayed within the |
| `ButtonControlDefinition` | ControlDefinition | Represents the information used to define a button. This isn't the visible button control but |
| `ButtonRowCommandInput` | CommandInput | Provides a command input to get a selection of a single button from a row of buttons. |
| `CameraEvent` | Event | A CameraEvent represents an event that occurs in reaction to the user manipulating the view. |
| `CameraEventArgs` | EventArgs | The CameraEventArgs provides information associated with a camera change. |
| `CheckBoxControlDefinition` | ControlDefinition | Represents the information used to define a check box. This isn't the visible check box control but |
| `ChoiceProperty` | Property | A property that is a predefined list of choices. |
| `Circle2D` | Curve2D | Transient 2D circle. A transient circle is not displayed or saved in a document. |
| `Circle3D` | Curve3D | Transient 3D circle. A transient circle is not displayed or saved in a document. |
| `ColorProperty` | Property | A property that defines a color. |
| `CommandControl` | ToolbarControl | Represents a button, check box, or radio control list in a panel, toolbar, or drop-down. |
| `CommandCreatedEvent` | Event | Class that needs to be implemented in order to respond to the CommandCreatedEvent event. |
| `CommandCreatedEventArgs` | EventArgs | Provides data for the CommandCreated event. |
| `CommandEvent` | Event | An event endpoint that supports the connection to client implemented CommandEventHandlers. |
| `CommandEventArgs` | EventArgs | Provides a set of arguments from a firing CommandEvent to a CommandEventHandler's notify callback method. |
| `Cone` | Surface | Transient cone. A transient cone is not displayed or saved in a document. |
| `CopyDesignFileInput` | CopyFileInput | Input object that defines the settings that apply when copying a design file, |
| `CustomEvent` | Event | A CustomEvent is primarily used to send an event from a worker thread you've created back |
| `CustomEventArgs` | EventArgs | The ApplicationEventArgs provides information associated with an application event. |
| `Cylinder` | Surface | Transient cylinder. A transient cylinder is not displayed or saved in a document. |
| `DataEvent` | Event | A Data event is an event associated with operations on Data items. |
| `DataEventArgs` | EventArgs | The DataEventArgs provides information associated with a data event. |
| `DataObjectFuture` | Future | Used to check the state of getting data associated with an object where the associated data |
| `DirectionCommandInput` | CommandInput | Represents a command input that gets a direction from the user. This displays |
| `DistanceValueCommandInput` | CommandInput | Represents a command input that gets a distance from the user. This displays |
| `DocumentEvent` | Event | A DocumentEvent represents a document related event. For example, DocumentOpening or DocumentOpened. |
| `DocumentEventArgs` | EventArgs | The DocumentEventArgs provides information associated with a document event. |
| `DropDownCommandInput` | CommandInput | Provides a command input to get the choice in a drop-down list from the user. |
| `DropDownControl` | ToolbarControl | Represents a drop-down control. |
| `DXF2DImportOptions` | ImportOptions | Defines that a 2D DXF Import to create sketches (based on layers in the DXF file) is to be performed and |
| `Ellipse2D` | Curve2D | Transient 2D ellipse. A transient ellipse is not displayed or saved in a document. |
| `Ellipse3D` | Curve3D | Transient 3D ellipse. A transient ellipse is n0t displayed or saved in a document. |
| `EllipticalArc2D` | Curve2D | Transient 2D elliptical arc. A transient elliptical arc is not displayed or saved in a document. |
| `EllipticalArc3D` | Curve3D | Transient 3D elliptical arc. A transient elliptical arc is not displayed or saved in a document. |
| `EllipticalCone` | Surface | Transient elliptical cone. A transient elliptical cone is not displayed or saved in a document. |
| `EllipticalCylinder` | Surface | Transient elliptical cylinder. A transient elliptical cylinder is not displayed or saved |
| `FilenameProperty` | Property | A property that defines a filename. |
| `FloatProperty` | Property | A float or real value property. |
| `FloatSpinnerCommandInput` | CommandInput | Provides a command input to get the value of a spinner from the user, the value type is float. |
| `FusionArchiveImportOptions` | ImportOptions | Defines that a Fusion Archive import is to be done and specifies the various options. |
| `GroupCommandInput` | CommandInput | Group Command inputs organize a set of command inputs into a collapsible |
| `HTMLEvent` | Event | A HTMLEvent is fired when triggered from JavaScript code associated with HTML used |
| `HTMLEventArgs` | EventArgs | The HTMLEventArgs provides access to the information sent from the JavaScript |
| `HttpEvent` | Event | A HttpEvent represents an event that occurs in reaction to a http request. |
| `HttpEventArgs` | EventArgs | The HttpEventArgs provides information associated with a http request. |
| `IGESImportOptions` | ImportOptions | Defines that an IGES import is to be done and specifies the various options. |
| `ImageCommandInput` | CommandInput | Provides an image command input for including an image in a command dialog. |
| `InfiniteLine3D` | Curve3D | Transient 3D infinite line. An infinite line is defined by a position and direction in space |
| `InputChangedEvent` | Event | An event endpoint that supports the connection to client implemented InputChangedEventHandlers. |
| `InputChangedEventArgs` | EventArgs | Provides a set of arguments from a firing InputChangedEvent to a InputEventChangedEventHandler's notify callback method. |
| `IntegerProperty` | Property | An integer value property. |
| `IntegerSpinnerCommandInput` | CommandInput | Provides a command input to get the value of a spinner from the user, the value type is integer. |
| `KeyboardEvent` | Event | An event endpoint that supports the connection to client implemented KeyboardEventHandlers. |
| `KeyboardEventArgs` | EventArgs | Provides a set of arguments from a firing KeyboardEvent to a KeyboardEventHandler's notify callback method. |
| `Line2D` | Curve2D | Transient 2D line. A transient line is not displayed or saved in a document. |
| `Line3D` | Curve3D | Transient 3D line. A transient line is not displayed or saved in a document. |
| `ListControlDefinition` | ControlDefinition | Represents the information used to define a list of check boxes, radio buttons, or text with icons. This class |
| `MarkingMenuEvent` | Event | A MarkingMenuEvent is fired when the marking menu and context menu are displayed. For example, in response to the |
| `MarkingMenuEventArgs` | EventArgs | The MarkingMenuEventArgs provides information associated with the marking and context |
| `MFGDMDataEvent` | Event | A MFGDMDataEvent represents an event related to the state of the MFGDM data structure. |
| `MFGDMDataEventArgs` | EventArgs | The MFGDMDataEventArgs provides information associated with the MFGDM event. |
| `MouseEvent` | Event | An event endpoint that supports the connection to client implemented MouseEventHandlers. |
| `MouseEventArgs` | EventArgs | Provides a set of arguments from a firing MouseEvent to a MouseEventHandler's notify callback method. |
| `NavigationEvent` | Event | A NavigationEvent is fired when a link is navigated on the page in a palette. |
| `NavigationEventArgs` | EventArgs | The NavigationEventArgs provides access to the information sent from the browser |
| `NurbsCurve2D` | Curve2D | Transient 2D NURBS curve. A transient NURBS curve is not displayed or saved in a document. |
| `NurbsCurve3D` | Curve3D | Transient 3D NURBS curve. A transient NURBS curve is not displayed or saved in a document. |
| `NurbsSurface` | Surface | Transient NURBS surface. A transient NURBS surface is not displayed or saved in a document. |
| `Plane` | Surface | Transient plane. A transient plane is not displayed or saved in a document. |
| `Polyline2D` | Curve2D | Represents a single curve composed of a series of connected lines in 2D space. |
| `Polyline3D` | Curve3D | Represents a single piecewise linear curve. This is a single curve that |
| `ProjectedTextureMapControl` | TextureMapControl | Provides access to the settings that control how a projected texture is applied to a body, |
| `RadioButtonGroupCommandInput` | CommandInput | Provides a command input to get the choice from a radio button group from the user. |
| `SATImportOptions` | ImportOptions | Defines that a SAT import is to be done and specifies the various options. |
| `SelectionCommandInput` | CommandInput | Provides a command input to get a selection from the user. |
| `SelectionEvent` | Event | An event endpoint that supports the connection to client implemented SelectionEventHandlers. |
| `SelectionEventArgs` | EventArgs | Provides a set of arguments from a firing SelectionEvent to a SelectionEventHandler's notify callback method. |
| `SeparatorCommandInput` | CommandInput | An object that represents a visual separator within a command dialog. |
| `SeparatorControl` | ToolbarControl | Represents a separator within a panel, toolbar, or drop-down control. |
| `SliderCommandInput` | CommandInput | Provides a command input to get the value of a slider from the user. |
| `SMTImportOptions` | ImportOptions | Defines that an SMT import is to be done and specifies the various options. |
| `Sphere` | Surface | Transient sphere. A transient sphere is not displayed or saved in a document. |
| `SplitButtonControl` | ToolbarControl | A split button has two active areas that the user can click; |
| `STEPImportOptions` | ImportOptions | Defines that a STEP import is to be done and specifies the various options. |
| `StringProperty` | Property | A string value property. |
| `StringValueCommandInput` | CommandInput | Provides a command input to get a string value from the user. |
| `SVGImportOptions` | ImportOptions | Defines that an SVG import is to be done and specifies the various options. |
| `TabCommandInput` | CommandInput | Tab command inputs contain a set of command inputs and/or group command inputs/ |
| `TableCommandInput` | CommandInput | Represents a table within a command dialog. The table consists of |
| `TextBoxCommandInput` | CommandInput | Provides a command input to interact with a text box. |
| `TextCommandPalette` | Palette | Represents the palette that is the Text Command window in Fusion. |
| `TextureMapControl3D` | TextureMapControl | Provides access to the settings that control how a 3D texture is applied to a body, |
| `Torus` | Surface | Transient torus. A transient torus is not displayed or saved in a document. |
| `TriadCommandInput` | CommandInput | Represents a command input that displays a triad and allows the user to control translation |
| `UserInterfaceGeneralEvent` | Event | A UserInterfaceGeneralEvent is used for user-interface related events that don't |
| `UserInterfaceGeneralEventArgs` | EventArgs | The UserInterfaceGeneralEventArgs is passed when a UserInterfaceGeneralEvent is fired. |
| `ValidateInputsEvent` | Event | An event endpoint that supports the connection to client implemented ValidateInputsEventHandlers. |
| `ValidateInputsEventArgs` | EventArgs | Provides a set of arguments from a firing ValidateInputsEvent to a ValidateInputsEventHandler's notify callback method. |
| `ValueCommandInput` | CommandInput | Provides a command input to get a unit based value from the user. |
| `WebRequestEvent` | Event | A WebRequestEvent represents an event that occurs in reaction to a Fusion protocol handler |
| `WebRequestEventArgs` | EventArgs | The WebRequestEventArgs provides information associated with a web request event. These |
| `WorkspaceEvent` | Event | A WorkspaceEvent represents a workspace related event. For example, workspaceActivate or workspaceDeactivate. |
| `WorkspaceEventArgs` | EventArgs | The WorkspaceEventArgs provides information associated with a workspace event. |
| `FloatSliderCommandInput` | SliderCommandInput | Provides a command input to get the value of a slider from the user, the value type is float. |
| `IntegerSliderCommandInput` | SliderCommandInput | Provides a command input to get the value of a slider from the user, the value type is integer. |
