# <a id="DotNetBrowser_Handlers_IHandler_2"></a> Interface IHandler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The common interface for all handlers.

```csharp
public interface IHandler<in TParameters, out TResponse>
```

#### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The result type.

## Methods

### <a id="DotNetBrowser_Handlers_IHandler_2_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
TResponse Handle(TParameters parameters)
```

#### Parameters

`parameters` TParameters

The handler parameters.

#### Returns

 TResponse

An object that represents the response that should be
determined based on the provided parameters.

