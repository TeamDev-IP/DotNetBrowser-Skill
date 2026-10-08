# <a id="DotNetBrowser_Input_Keyboard_IKeyboard"></a> Interface IKeyboard

Namespace: [DotNetBrowser.Input.Keyboard](DotNetBrowser.Input.Keyboard.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for keyboard input simulation and handling.

```csharp
public interface IKeyboard : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Input_Keyboard_IKeyboard_KeyPressed"></a> KeyPressed

Occurs when a key is pressed for the browser. This corresponds to <code>KeyDown</code> event of WPF and WinForms
controls.

```csharp
IInterceptableInputEvent<IKeyPressedEventArgs, KeyPressedEventArgs> KeyPressed { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IKeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyPressedEventArgs.md), [KeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyPressedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Keyboard_IKeyboard_KeyReleased"></a> KeyReleased

Occurs when a key is released for the browser. This corresponds to <code>KeyUp</code> event of WPF and WinForms controls.

```csharp
IInterceptableInputEvent<IKeyReleasedEventArgs, KeyReleasedEventArgs> KeyReleased { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IKeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyReleasedEventArgs.md), [KeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyReleasedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Keyboard_IKeyboard_KeyTyped"></a> KeyTyped

Occurs when a control code, character, space, enter or backspace key is pressed for the browser.
This corresponds to <code>KeyPress</code> event of WinForms controls.

```csharp
IInterceptableInputEvent<IKeyTypedEventArgs, KeyTypedEventArgs> KeyTyped { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IKeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyTypedEventArgs.md), [KeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyTypedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

