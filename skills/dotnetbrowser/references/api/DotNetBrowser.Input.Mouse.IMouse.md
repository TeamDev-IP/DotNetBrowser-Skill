# <a id="DotNetBrowser_Input_Mouse_IMouse"></a> Interface IMouse

Namespace: [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for mouse input simulation and handling.

```csharp
public interface IMouse : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[MouseExtensions.SimulateClick\(IMouse, MouseButton, Point\)](DotNetBrowser.Input.Mouse.MouseExtensions.md\#DotNetBrowser\_Input\_Mouse\_MouseExtensions\_SimulateClick\_DotNetBrowser\_Input\_Mouse\_IMouse\_DotNetBrowser\_Input\_Mouse\_Events\_MouseButton\_DotNetBrowser\_Geometry\_Point\_), 
[MouseExtensions.SimulateClick\(IMouse, MouseButton, IElement\)](DotNetBrowser.Input.Mouse.MouseExtensions.md\#DotNetBrowser\_Input\_Mouse\_MouseExtensions\_SimulateClick\_DotNetBrowser\_Input\_Mouse\_IMouse\_DotNetBrowser\_Input\_Mouse\_Events\_MouseButton\_DotNetBrowser\_Dom\_IElement\_)

## Properties

### <a id="DotNetBrowser_Input_Mouse_IMouse_Dragged"></a> Dragged

Gets the mouse dragged event for the browser.

```csharp
IInputEvent<IMouseDraggedEventArgs, MouseDraggedEventArgs> Dragged { get; }
```

#### Property Value

 [IInputEvent](DotNetBrowser.Input.IInputEvent\-2.md)<[IMouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseDraggedEventArgs.md), [MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseDraggedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_Entered"></a> Entered

Occurs when the mouse has entered the web page.

```csharp
IInterceptableInputEvent<IMouseEnteredEventArgs, MouseEnteredEventArgs> Entered { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEnteredEventArgs.md), [MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEnteredEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_Exited"></a> Exited

Occurs when the mouse has exited the web page.

```csharp
IInterceptableInputEvent<IMouseExitedEventArgs, MouseExitedEventArgs> Exited { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseExitedEventArgs.md), [MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseExitedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_Moved"></a> Moved

Occurs when the mouse has moved over the web page.

```csharp
IInterceptableInputEvent<IMouseMovedEventArgs, MouseMovedEventArgs> Moved { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseMovedEventArgs.md), [MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseMovedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_Pressed"></a> Pressed

Occurs when the mouse button has been pressed on the web page.

```csharp
IInterceptableInputEvent<IMousePressedEventArgs, MousePressedEventArgs> Pressed { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.IMousePressedEventArgs.md), [MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.MousePressedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_Released"></a> Released

Occurs when the mouse button has been released on the web page.

```csharp
IInterceptableInputEvent<IMouseReleasedEventArgs, MouseReleasedEventArgs> Released { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseReleasedEventArgs.md), [MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseReleasedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Mouse_IMouse_WheelMoved"></a> WheelMoved

Occurs when the mouse wheel has scrolled on the web page.

```csharp
IInterceptableInputEvent<IMouseWheelMovedEventArgs, MouseWheelMovedEventArgs> WheelMoved { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[IMouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseWheelMovedEventArgs.md), [MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseWheelMovedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

