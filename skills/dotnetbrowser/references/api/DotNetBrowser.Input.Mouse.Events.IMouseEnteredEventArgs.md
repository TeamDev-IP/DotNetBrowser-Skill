# <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs"></a> Interface IMouseEnteredEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Entered" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseEnteredEventArgs : IMouseEventArgs
```

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_Button"></a> Button

Gets the mouse button that is pressed when entering the browser.

```csharp
MouseButton Button { get; }
```

#### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.MouseButton.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

#### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md)

