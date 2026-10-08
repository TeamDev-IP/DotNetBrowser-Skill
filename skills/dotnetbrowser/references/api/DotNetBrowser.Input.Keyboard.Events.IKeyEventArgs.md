# <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs"></a> Interface IKeyEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The base interface of all event arguments for the key events.

```csharp
public interface IKeyEventArgs
```

## Properties

### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_KeyLocation"></a> KeyLocation

Gets the key location on the keyboard.

```csharp
KeyLocation KeyLocation { get; }
```

#### Property Value

 [KeyLocation](DotNetBrowser.Input.Keyboard.Events.KeyLocation.md)

### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_Modifiers"></a> Modifiers

Gets the key modifiers.

```csharp
IKeyModifiers Modifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_VirtualKey"></a> VirtualKey

Gets the virtual key code.

```csharp
KeyCode VirtualKey { get; }
```

#### Property Value

 [KeyCode](DotNetBrowser.Input.Keyboard.Events.KeyCode.md)

