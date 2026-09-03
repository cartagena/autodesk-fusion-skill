# Class index: adsk.volume

30 classes/enums found in `references/api-stubs/volume.py`. Use `grep -n "^class ClassName" references/api-stubs/volume.py` to jump to a definition.

| Class | Base | Summary |
|---|---|---|
| `ControlPointInterpolators` |  | Types of interpolation functions for the control point maps. |
| `GraphOutputNodeTypes` |  | Types of graph output nodes for the main graph. |
| `GraphTypes` |  | Graph types for a volumetric model. |
| `NodePinTypes` |  | Different types that graph nodes input and output types can be. |
| `BeamNetwork` | core.Base | A geometry reference property that defines a BeamNetwork object which is |
| `ColorControlPoint` | core.Base | A read-only structure that represents a control point used in ColorControlPointMapGraphNodeProperty. |
| `CustomSDFCallbackEventHandler` | core.EventHandler | API clients can implement subclasses of this handler to enable custom Signed Distance Field geometries. |
| `Graph` | core.Base | The graph that describes the volumetric model. |
| `GraphConnector` | core.Base | A simple read-only structure that represents a connection beween two nodes' pins in the graph. |
| `GraphNode` | core.Base | An individual node within a graph. |
| `GraphNodeProperties` | core.Base | A collection of properties of a graph node. |
| `GraphNodeProperty` | core.Base | Class for representing a property of a graph node. These can be of many types. |
| `ScalarControlPoint` | core.Base | A read-only structure that represents a control point used in ScalarControlPointMapGraphNodeProperty. |
| `VolumetricModel` | core.Base | The main volumetric graph object. It has a parent component and is defined in this parent component's space. |
| `VolumetricSample` | core.Base | The VolumetricSamples object which is a base class for containing the result of sampling the volumetric model an array of points. |
| `VolumetricSampler` | core.Base | The VolumetricSampler object which is used for controled sampling of the volumetric model. |
| `BooleanGraphNodeProperty` | GraphNodeProperty | A property value that is a boolean. |
| `ColorControlPointMapGraphNodeProperty` | GraphNodeProperty | A property value that defines a complex mapping curve from an input domain of double values to |
| `ColorGraphNodeProperty` | GraphNodeProperty | A property value that is a color. |
| `GeometryGraphNodeProperty` | GraphNodeProperty | A property value that represents a link to a geometric object. |
| `IntegerGraphNodeProperty` | GraphNodeProperty | A property value that is an integer. |
| `Matrix3DGraphNodeProperty` | GraphNodeProperty | A property value that is a 3D Matrix. |
| `ScalarControlPointMapGraphNodeProperty` | GraphNodeProperty | A property value that defines a complex mapping curve from an input domain of double values to |
| `ScalarGraphNodeProperty` | GraphNodeProperty | A property value that is a floating point value. |
| `StringGraphNodeProperty` | GraphNodeProperty | A property value that is a string. |
| `TransformRefGraphNodeProperty` | GraphNodeProperty | A property value that is provides a transform to a node. This is set with an Occurrence of a Component. |
| `Vector3DGraphNodeProperty` | GraphNodeProperty | A property value that is a 3D vector. |
| `VolumetricColorSample` | VolumetricSample | The VolumetricColorSample object which contains the result of sampling a color value from the volumetric model at a point. |
| `VolumetricScalarSample` | VolumetricSample | The VolumetricScalarSample object which contains the result of sampling a scalar value from the volumetric model at a point. |
| `VolumetricVectorSample` | VolumetricSample | The VolumetricVectorSample object which contains the result of sampling a vector value from the volumetric model at a point. |
