# <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs"></a> Interface IMouseMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseMovedEventArgs : IMouseEventArgs
```

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_Button"></a> Button

Gets the mouse button that is pressed during the move.

```csharp
MouseButton Button { get; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

