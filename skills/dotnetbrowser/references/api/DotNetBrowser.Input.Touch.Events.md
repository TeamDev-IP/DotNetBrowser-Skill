# <a id="DotNetBrowser_Input_Touch_Events"></a> Namespace DotNetBrowser.Input.Touch.Events

### Classes

 [TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs)

 [TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs)

 [TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs)

 [TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs)

 [TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)

 [TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs)

### Interfaces

 [ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

Event arguments for the <xref href="DotNetBrowser.Input.Touch.ITouch" data-throw-if-not-resolved="false"></xref> events associated with a surface touch.

 [ITouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchPoint)

A single contact point on a touch-sensitive device.

### Enums

 [TouchState](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchState)

The possible states of the touch point.

## <a id="DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs"></a> Class TouchCanceledEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchCanceledEventArgs : TouchEventArgs, ITouchEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs) ← 
[TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs)

##### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

##### Inherited Members

[TouchEventArgs.KeyModifiers](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers), 
[TouchEventArgs.TouchPoints](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints), 
[TouchEventArgs.Equals\(object\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_), 
[TouchEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs__ctor_DotNetBrowser_Input_Touch_Events_TouchPoint___"></a> TouchCanceledEventArgs\(params TouchPoint\[\]\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchCanceledEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchCanceledEventArgs(params TouchPoint[] points)
```

##### Parameters

`points` [TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\[\]

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchCanceledEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchCanceledEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchCanceledEventArgs(IEnumerable<TouchPoint> points)
```

##### Parameters

`points` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\>

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

If no points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

If  <code class="paramref">points</code> is null.

## <a id="DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs"></a> Class TouchEndedEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchEndedEventArgs : TouchEventArgs, ITouchEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs) ← 
[TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs)

##### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

##### Inherited Members

[TouchEventArgs.KeyModifiers](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers), 
[TouchEventArgs.TouchPoints](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints), 
[TouchEventArgs.Equals\(object\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_), 
[TouchEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs__ctor_DotNetBrowser_Input_Touch_Events_TouchPoint___"></a> TouchEndedEventArgs\(params TouchPoint\[\]\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchEndedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchEndedEventArgs(params TouchPoint[] points)
```

##### Parameters

`points` [TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\[\]

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchEndedEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchEndedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchEndedEventArgs(IEnumerable<TouchPoint> points)
```

##### Parameters

`points` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\>

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

## <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs"></a> Class TouchEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public abstract class TouchEventArgs : ITouchEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs)

##### Derived

[TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs), 
[TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs), 
[TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs), 
[TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs)

##### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of <xref href="DotNetBrowser.Input.Touch.Events.TouchEventArgs" data-throw-if-not-resolved="false"></xref>.

```csharp
protected TouchEventArgs(IEnumerable<TouchPoint> touchPoints)
```

##### Parameters

`touchPoints` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\>

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

### Properties

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints"></a> TouchPoints

Gets the list of all detected touch points.

```csharp
public IReadOnlyList<ITouchPoint> TouchPoints { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchPoint)\>

### Methods

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs"></a> Class TouchMovedEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchMovedEventArgs : TouchEventArgs, ITouchEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs) ← 
[TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs)

##### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

##### Inherited Members

[TouchEventArgs.KeyModifiers](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers), 
[TouchEventArgs.TouchPoints](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints), 
[TouchEventArgs.Equals\(object\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_), 
[TouchEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs__ctor_DotNetBrowser_Input_Touch_Events_TouchPoint___"></a> TouchMovedEventArgs\(params TouchPoint\[\]\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchMovedEventArgs(params TouchPoint[] points)
```

##### Parameters

`points` [TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\[\]

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchMovedEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchMovedEventArgs(IEnumerable<TouchPoint> points)
```

##### Parameters

`points` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\>

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

## <a id="DotNetBrowser_Input_Touch_Events_TouchPoint"></a> Class TouchPoint

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchPoint : ITouchPoint
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)

##### Implements

[ITouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchPoint)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint__ctor_System_Int32_DotNetBrowser_Input_Touch_Events_TouchState_DotNetBrowser_Geometry_Point_"></a> TouchPoint\(int, TouchState, Point\)

Initializes a new instance of <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint" data-throw-if-not-resolved="false"></xref> with the specified identifier, state, and
location.

```csharp
public TouchPoint(int id, TouchState state, Point locationOnWidget)
```

##### Parameters

`id` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The touch point identifier. If this instance denotes a new touch point, its identifier should be a
unique integer value.If this instance denotes an already existing point that we want to move, end or cancel,
its identifier should be equal to the identifier of that existing touch point.

`state` [TouchState](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchState)

The state of the touch point.

`locationOnWidget` [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

The position relative to the bounds of the widget.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">locationOnWidget</code> is null.

### Properties

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Force"></a> Force

Gets the amount of pressure being applied to the surface.

```csharp
public float? Force { get; set; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)?

##### Remarks

Can be null if force detection is not supported.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Id"></a> Id

Gets the touch point unique identifier.

```csharp
public int Id { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

Every touch has a constant identifier while a finger touches the surface and it stay the same during of its holding
or movement around the surface. Removing any count of touches from the surface doesn't change the identifiers of
remaining
touches.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_LocationOnScreen"></a> LocationOnScreen

Gets the touch point location relative to the bounds of the screen.

```csharp
public Point LocationOnScreen { get; set; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_LocationOnWidget"></a> LocationOnWidget

Gets or sets the position relative to the bounds of the widget.

```csharp
public Point LocationOnWidget { get; set; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint.LocationOnWidget" data-throw-if-not-resolved="false"></xref> can't be null.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_TouchEllipse"></a> TouchEllipse

Gets or sets the touch ellipse that most closely circumscribes the area of contact with the screen.

```csharp
public Ellipse TouchEllipse { get; set; }
```

##### Property Value

 [Ellipse](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Ellipse)

##### Remarks

The touch ellipse approximates the size and shape of the area of contact between the user and the screen.
It consists from the major X axis length, the major Y axis length and the touch ellipse rotation angle.
The rotation angle is an angle, in degrees, of the contact area ellipse defined by
<xref href="DotNetBrowser.Geometry.Ellipse.RadiusX" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Geometry.Ellipse.RadiusY" data-throw-if-not-resolved="false"></xref>. The value may be between 0 and 90.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <xref href="DotNetBrowser.Input.Touch.Events.TouchPoint.TouchEllipse" data-throw-if-not-resolved="false"></xref> can't be null.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The angle of touch ellipse out of range 0-90 degrees.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_TouchState"></a> TouchState

Gets the current state of touch.

```csharp
public TouchState TouchState { get; set; }
```

##### Property Value

 [TouchState](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchState)

### Methods

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Touch_Events_TouchPoint_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs"></a> Class TouchStartedEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchStartedEventArgs : TouchEventArgs, ITouchEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs) ← 
[TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs)

##### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs)

##### Inherited Members

[TouchEventArgs.KeyModifiers](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers), 
[TouchEventArgs.TouchPoints](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints), 
[TouchEventArgs.Equals\(object\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_), 
[TouchEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs__ctor_DotNetBrowser_Input_Touch_Events_TouchPoint___"></a> TouchStartedEventArgs\(params TouchPoint\[\]\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchStartedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchStartedEventArgs(params TouchPoint[] points)
```

##### Parameters

`points` [TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\[\]

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

#### <a id="DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchStartedEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchStartedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchStartedEventArgs(IEnumerable<TouchPoint> points)
```

##### Parameters

`points` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchPoint)\>

The touch points to add.

##### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

## <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs"></a> Interface ITouchEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Touch.ITouch" data-throw-if-not-resolved="false"></xref> events associated with a surface touch.

```csharp
public interface ITouchEventArgs
```

### Properties

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs_TouchPoints"></a> TouchPoints

Gets the list of all detected touch points.

```csharp
IReadOnlyList<ITouchPoint> TouchPoints { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchPoint)\>

## <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint"></a> Interface ITouchPoint

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

A single contact point on a touch-sensitive device.

```csharp
public interface ITouchPoint
```

### Properties

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_Force"></a> Force

Gets the amount of pressure being applied to the surface.

```csharp
float? Force { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)?

##### Remarks

Can be null if force detection is not supported.

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_Id"></a> Id

Gets the touch point unique identifier.

```csharp
int Id { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

Every touch has a constant identifier while a finger touches the surface and it stay the same during of its holding
or movement around the surface. Removing any count of touches from the surface doesn't change the identifiers of
remaining
touches.

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_LocationOnScreen"></a> LocationOnScreen

Gets the touch point location relative to the bounds of the screen.

```csharp
Point LocationOnScreen { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_LocationOnWidget"></a> LocationOnWidget

Gets the touch point location relative to the bounds of the widget.

```csharp
Point LocationOnWidget { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_TouchEllipse"></a> TouchEllipse

Gets the touch ellipse that most closely circumscribes the area of contact with the screen.

```csharp
Ellipse TouchEllipse { get; }
```

##### Property Value

 [Ellipse](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Ellipse)

##### Remarks

It consists from the major X axis length, the major Y axis length and the touch ellipse rotation angle.
Together, these three values describe an ellipse that approximates the size and shape of the area of contact
between the user and the screen.
The rotation angle is an angle, in degrees, of the contact area ellipse defined by
<xref href="DotNetBrowser.Geometry.Ellipse.RadiusX" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Geometry.Ellipse.RadiusY" data-throw-if-not-resolved="false"></xref>. The value may be between 0 and 90.

#### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_TouchState"></a> TouchState

Gets the current state of touch.

```csharp
TouchState TouchState { get; }
```

##### Property Value

 [TouchState](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchState)

## <a id="DotNetBrowser_Input_Touch_Events_TouchState"></a> Enum TouchState

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

The possible states of the touch point.

```csharp
public enum TouchState
```

### Fields

`Canceled = 6` 

The touch has been canceled.



`Ended = 3` 

The touch has ended.



`Moved = 4` 

The touch point has moved.



`Started = 2` 

The touch has started.



`Stationary = 5` 

The touch point didn't change its state.



`Unknown = 1` 

The touch point state is unknown.
