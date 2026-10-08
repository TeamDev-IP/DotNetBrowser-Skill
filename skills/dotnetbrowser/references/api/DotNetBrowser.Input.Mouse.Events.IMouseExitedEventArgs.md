# <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs"></a> Interface IMouseExitedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseExitedEventArgs : IMouseEventArgs
```

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_Button"></a> Button

Gets the mouse button that is pressed when exiting the browser.

```csharp
MouseButton Button { get; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

