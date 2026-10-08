# <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs"></a> Class MouseExitedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseExitedEventArgs : MouseEventArgs, IMouseExitedEventArgs, IMouseEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md) ← 
[MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseExitedEventArgs.md)

#### Implements

[IMouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseExitedEventArgs.md), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

#### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Equals\_System\_Object\_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_Button"></a> Button

Gets or sets the mouse button that is pressed when exiting the browser.

```csharp
public MouseButton Button { get; set; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

