# <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs"></a> Class MouseButtonEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

```csharp
public class MouseButtonEventArgs : MouseEventArgs, IMouseButtonEventArgs, IMouseEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md) ← 
[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.MouseButtonEventArgs.md)

#### Derived

[MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.MousePressedEventArgs.md), 
[MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseReleasedEventArgs.md)

#### Implements

[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseButtonEventArgs.md), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

#### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Equals\_System\_Object\_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_GetHashCode), 
[MouseEventArgs.Equals\(MouseEventArgs\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Equals\_DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_Button"></a> Button

Gets or sets the mouse button this event is related to.

```csharp
public MouseButton Button { get; set; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_ClickCount"></a> ClickCount

Gets or sets the count of consecutive clicks that happened in a short amount of time.

```csharp
public uint ClickCount { get; set; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

