# <a id="DotNetBrowser_Input"></a> Namespace DotNetBrowser.Input

### Namespaces

 [DotNetBrowser.Input.DragAndDrop](DotNetBrowser.Input.DragAndDrop.md)

 [DotNetBrowser.Input.Keyboard](DotNetBrowser.Input.Keyboard.md)

 [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)

 [DotNetBrowser.Input.Touch](DotNetBrowser.Input.Touch.md)

### Interfaces

 [IInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.md#DotNetBrowser_Input_IInputEvent_2)

An input event. It is possible to raise this input event and dispatch it to the currently loaded web page.

 [IInterceptableEvent<TIInputEventArgs\>](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableEvent_1)

An interceptable input event. It is possible to intercept and suppress this input event before it is actually
processed by the browser.

 [IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)

An interceptable and raisable input event. It is possible to intercept and
suppress this input event before it is actually processed by the browser
or to raise it and dispatch to the currently loaded web page.

### Enums

 [InputEventResponse](DotNetBrowser.Input.md#DotNetBrowser_Input_InputEventResponse)

The response to the input event handlers.

## <a id="DotNetBrowser_Input_IInputEvent_2"></a> Interface IInputEvent<TIInputEventArgs, TInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An input event. It is possible to raise this input event and dispatch it to the currently loaded web page.

```csharp
public interface IInputEvent<TIInputEventArgs, in TInputEventArgs> where TInputEventArgs : TIInputEventArgs
```

##### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

`TInputEventArgs` 

The input event arguments.

### Methods

#### <a id="DotNetBrowser_Input_IInputEvent_2_Raise__1_"></a> Raise\(TInputEventArgs\)

Raises and dispatches the event to the currently loaded web page. It does nothing if the
browser hasn't loaded any web page.

```csharp
void Raise(TInputEventArgs args)
```

##### Parameters

`args` TInputEventArgs

The event arguments.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The corresponding browser object has already been disposed.

## <a id="DotNetBrowser_Input_IInterceptableEvent_1"></a> Interface IInterceptableEvent<TIInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An interceptable input event. It is possible to intercept and suppress this input event before it is actually
processed by the browser.

```csharp
public interface IInterceptableEvent<TIInputEventArgs>
```

##### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

### Properties

#### <a id="DotNetBrowser_Input_IInterceptableEvent_1_Handler"></a> Handler

Gets or sets the event handler that can be used to intercept and/or suppress this input event.

```csharp
IHandler<TIInputEventArgs, InputEventResponse> Handler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<TIInputEventArgs, [InputEventResponse](DotNetBrowser.Input.md#DotNetBrowser_Input_InputEventResponse)\>

## <a id="DotNetBrowser_Input_IInterceptableInputEvent_2"></a> Interface IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An interceptable and raisable input event. It is possible to intercept and
suppress this input event before it is actually processed by the browser
or to raise it and dispatch to the currently loaded web page.

```csharp
public interface IInterceptableInputEvent<TIInputEventArgs, in TInputEventArgs> : IInterceptableEvent<TIInputEventArgs>, IInputEvent<TIInputEventArgs, TInputEventArgs> where TInputEventArgs : TIInputEventArgs
```

##### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

`TInputEventArgs` 

The input event arguments.

##### Implements

[IInterceptableEvent<TIInputEventArgs\>](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableEvent_1), 
[IInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.md#DotNetBrowser_Input_IInputEvent_2)

## <a id="DotNetBrowser_Input_InputEventResponse"></a> Enum InputEventResponse

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

The response to the input event handlers.

```csharp
public enum InputEventResponse
```

### Fields

`Proceed = 1` 

Allow the browser to process this event.



`Suppress = 0` 

Suppress this event.
