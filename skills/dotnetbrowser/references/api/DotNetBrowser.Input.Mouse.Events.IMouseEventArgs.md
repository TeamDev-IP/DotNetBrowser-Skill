# <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs"></a> Interface IMouseEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The base interface for all <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public interface IMouseEventArgs
```

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs_Location"></a> Location

Gets the mouse position relative to the bounds of the browser instance.

```csharp
Point Location { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs_LocationOnScreen"></a> LocationOnScreen

Gets the mouse position relative to the bounds of the screen.

```csharp
Point LocationOnScreen { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

