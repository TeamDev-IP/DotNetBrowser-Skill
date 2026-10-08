# <a id="DotNetBrowser_Input"></a> Namespace DotNetBrowser.Input

### Namespaces

 [DotNetBrowser.Input.DragAndDrop](DotNetBrowser.Input.DragAndDrop.md)

 [DotNetBrowser.Input.Keyboard](DotNetBrowser.Input.Keyboard.md)

 [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)

 [DotNetBrowser.Input.Touch](DotNetBrowser.Input.Touch.md)

### Interfaces

 [IInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.IInputEvent\-2.md)

An input event. It is possible to raise this input event and dispatch it to the currently loaded web page.

 [IInterceptableEvent<TIInputEventArgs\>](DotNetBrowser.Input.IInterceptableEvent\-1.md)

An interceptable input event. It is possible to intercept and suppress this input event before it is actually
processed by the browser.

 [IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)

An interceptable and raisable input event. It is possible to intercept and
suppress this input event before it is actually processed by the browser
or to raise it and dispatch to the currently loaded web page.

### Enums

 [InputEventResponse](DotNetBrowser.Input.InputEventResponse.md)

The response to the input event handlers.

