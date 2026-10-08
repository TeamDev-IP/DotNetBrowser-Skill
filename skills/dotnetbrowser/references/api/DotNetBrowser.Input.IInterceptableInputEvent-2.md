# <a id="DotNetBrowser_Input_IInterceptableInputEvent_2"></a> Interface IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An interceptable and raisable input event. It is possible to intercept and
suppress this input event before it is actually processed by the browser
or to raise it and dispatch to the currently loaded web page.

```csharp
public interface IInterceptableInputEvent<TIInputEventArgs, in TInputEventArgs> : IInterceptableEvent<TIInputEventArgs>, IInputEvent<TIInputEventArgs, TInputEventArgs> where TInputEventArgs : TIInputEventArgs
```

#### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

`TInputEventArgs` 

The input event arguments.

#### Implements

[IInterceptableEvent<TIInputEventArgs\>](DotNetBrowser.Input.IInterceptableEvent\-1.md), 
[IInputEvent<TIInputEventArgs, TInputEventArgs\>](DotNetBrowser.Input.IInputEvent\-2.md)

