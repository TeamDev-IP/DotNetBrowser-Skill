# <a id="DotNetBrowser_Input_IInputEvent_2"></a> Interface IInputEvent<TIInputEventArgs, TInputEventArgs\>

Namespace: [DotNetBrowser.Input](DotNetBrowser.Input.md)  
Assembly: DotNetBrowser.dll  

An input event. It is possible to raise this input event and dispatch it to the currently loaded web page.

```csharp
public interface IInputEvent<TIInputEventArgs, in TInputEventArgs> where TInputEventArgs : TIInputEventArgs
```

#### Type Parameters

`TIInputEventArgs` 

The input event arguments interface.

`TInputEventArgs` 

The input event arguments.

## Methods

### <a id="DotNetBrowser_Input_IInputEvent_2_Raise__1_"></a> Raise\(TInputEventArgs\)

Raises and dispatches the event to the currently loaded web page. It does nothing if the
browser hasn't loaded any web page.

```csharp
void Raise(TInputEventArgs args)
```

#### Parameters

`args` TInputEventArgs

The event arguments.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The corresponding browser object has already been disposed.

