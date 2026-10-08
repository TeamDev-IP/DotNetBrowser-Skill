# <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint"></a> Interface ITouchPoint

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

A single contact point on a touch-sensitive device.

```csharp
public interface ITouchPoint
```

## Properties

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_Force"></a> Force

Gets the amount of pressure being applied to the surface.

```csharp
float? Force { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)?

#### Remarks

Can be null if force detection is not supported.

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_Id"></a> Id

Gets the touch point unique identifier.

```csharp
int Id { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Remarks

Every touch has a constant identifier while a finger touches the surface and it stay the same during of its holding
or movement around the surface. Removing any count of touches from the surface doesn't change the identifiers of
remaining
touches.

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_LocationOnScreen"></a> LocationOnScreen

Gets the touch point location relative to the bounds of the screen.

```csharp
Point LocationOnScreen { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_LocationOnWidget"></a> LocationOnWidget

Gets the touch point location relative to the bounds of the widget.

```csharp
Point LocationOnWidget { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_TouchEllipse"></a> TouchEllipse

Gets the touch ellipse that most closely circumscribes the area of contact with the screen.

```csharp
Ellipse TouchEllipse { get; }
```

#### Property Value

 [Ellipse](DotNetBrowser.Geometry.Ellipse.md)

#### Remarks

It consists from the major X axis length, the major Y axis length and the touch ellipse rotation angle.
Together, these three values describe an ellipse that approximates the size and shape of the area of contact
between the user and the screen.
The rotation angle is an angle, in degrees, of the contact area ellipse defined by
<xref href="DotNetBrowser.Geometry.Ellipse.RadiusX" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Geometry.Ellipse.RadiusY" data-throw-if-not-resolved="false"></xref>. The value may be between 0 and 90.

### <a id="DotNetBrowser_Input_Touch_Events_ITouchPoint_TouchState"></a> TouchState

Gets the current state of touch.

```csharp
TouchState TouchState { get; }
```

#### Property Value

 [TouchState](DotNetBrowser.Input.Touch.Events.TouchState.md)

