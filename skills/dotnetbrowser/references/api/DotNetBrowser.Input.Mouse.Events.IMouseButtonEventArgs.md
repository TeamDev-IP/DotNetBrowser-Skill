# <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs"></a> Interface IMouseButtonEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

```csharp
public interface IMouseButtonEventArgs : IMouseEventArgs
```

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_Button"></a> Button

Gets the mouse button this event is related to.

```csharp
MouseButton Button { get; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_ClickCount"></a> ClickCount

Gets the count of consecutive clicks that happened in a short amount of time.

```csharp
uint ClickCount { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

