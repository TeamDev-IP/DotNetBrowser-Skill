# <a id="DotNetBrowser_Input_Mouse_MouseExtensions"></a> Class MouseExtensions

Namespace: [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)  
Assembly: DotNetBrowser.Core.dll  

The mouse input simulation service extension methods.

```csharp
public static class MouseExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseExtensions](DotNetBrowser.Input.Mouse.MouseExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Geometry_Point_"></a> SimulateClick\(IMouse, MouseButton, Point\)

Simulate mouse button click at the specified location.

```csharp
public static void SimulateClick(this IMouse mouse, MouseButton mouseButton, Point location)
```

#### Parameters

`mouse` [IMouse](DotNetBrowser.Input.Mouse.IMouse.md)

The mouse input simulation service.

`mouseButton` [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

The mouse button that should be used for clicking.

`location` [Point](DotNetBrowser.Geometry.Point.md)

The mouse pointer location relative to the top left corner of the browser.

#### Remarks

The mouse click is simulated by raising <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref>, and
<xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> events in a sequence.

### <a id="DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Dom_IElement_"></a> SimulateClick\(IMouse, MouseButton, IElement\)

Simulate mouse button click at the specified element.

```csharp
public static void SimulateClick(this IMouse mouse, MouseButton mouseButton, IElement element)
```

#### Parameters

`mouse` [IMouse](DotNetBrowser.Input.Mouse.IMouse.md)

The mouse input simulation service.

`mouseButton` [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

The mouse button that should be used for clicking.

`element` [IElement](DotNetBrowser.Dom.IElement.md)

The element to click at.

#### Remarks

<p>
    The mouse click is simulated by raising <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref>, and
    <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> events in a sequence.
</p>
<p> The point to click at is determined as the center of the bounding client rectangle of the specified element.</p>

