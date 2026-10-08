# <a id="DotNetBrowser_Input_IInterceptableEvent_1"></a> Interface IInterceptableEvent<TIInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An interceptable input event. It is possible to intercept and suppress this input event before it is actually
processed by the browser.

```csharp
public interface IInterceptableEvent<TIInputEventArgs>
```

#### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

## Properties

### <a id="DotNetBrowser_Input_IInterceptableEvent_1_Handler"></a> Handler

Gets or sets the event handler that can be used to intercept and/or suppress this input event.

```csharp
IHandler<TIInputEventArgs, InputEventResponse> Handler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<TIInputEventArgs, [InputEventResponse](DotNetBrowser.Input.InputEventResponse.md)\>

