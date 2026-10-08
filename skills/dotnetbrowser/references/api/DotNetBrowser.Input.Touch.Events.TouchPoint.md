# <a id="DotNetBrowser_Input_Touch_Events_TouchPoint"></a> Class TouchPoint

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchPoint : ITouchPoint
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchPoint](DotNetBrowser.Input.Touch.Events.TouchPoint.md)

#### Implements

[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint__ctor_System_Int32_DotNetBrowser_Input_Touch_Events_TouchState_DotNetBrowser_Geometry_Point_"></a> TouchPoint\(int, TouchState, Point\)

Initializes a new instance of <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint" data-throw-if-not-resolved="false"></xref> with the specified identifier, state, and
location.

```csharp
public TouchPoint(int id, TouchState state, Point locationOnWidget)
```

#### Parameters

`id` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The touch point identifier. If this instance denotes a new touch point, its identifier should be a
unique integer value.If this instance denotes an already existing point that we want to move, end or cancel,
its identifier should be equal to the identifier of that existing touch point.

`state` [TouchState](DotNetBrowser.Input.Touch.Events.TouchState.md)

The state of the touch point.

`locationOnWidget` [Point](DotNetBrowser.Geometry.Point.md)

The position relative to the bounds of the widget.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">locationOnWidget</code> is null.

## Properties

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Force"></a> Force

Gets the amount of pressure being applied to the surface.

```csharp
public float? Force { get; set; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)?

#### Remarks

Can be null if force detection is not supported.

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Id"></a> Id

Gets the touch point unique identifier.

```csharp
public int Id { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Remarks

Every touch has a constant identifier while a finger touches the surface and it stay the same during of its holding
or movement around the surface. Removing any count of touches from the surface doesn't change the identifiers of
remaining
touches.

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_LocationOnScreen"></a> LocationOnScreen

Gets the touch point location relative to the bounds of the screen.

```csharp
public Point LocationOnScreen { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_LocationOnWidget"></a> LocationOnWidget

Gets or sets the position relative to the bounds of the widget.

```csharp
public Point LocationOnWidget { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint.LocationOnWidget" data-throw-if-not-resolved="false"></xref> can't be null.

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_TouchEllipse"></a> TouchEllipse

Gets or sets the touch ellipse that most closely circumscribes the area of contact with the screen.

```csharp
public Ellipse TouchEllipse { get; set; }
```

#### Property Value

 [Ellipse](DotNetBrowser.Geometry.Ellipse.md)

#### Remarks

The touch ellipse approximates the size and shape of the area of contact between the user and the screen.
It consists from the major X axis length, the major Y axis length and the touch ellipse rotation angle.
The rotation angle is an angle, in degrees, of the contact area ellipse defined by
<xref href="DotNetBrowser.Geometry.Ellipse.RadiusX" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Geometry.Ellipse.RadiusY" data-throw-if-not-resolved="false"></xref>. The value may be between 0 and 90.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint.TouchEllipse" data-throw-if-not-resolved="false"></xref> can't be null.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The angle of touch ellipse out of range 0-90 degrees.

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_TouchState"></a> TouchState

Gets the current state of touch.

```csharp
public TouchState TouchState { get; set; }
```

#### Property Value

 [TouchState](DotNetBrowser.Input.Touch.Events.TouchState.md)

## Methods

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

