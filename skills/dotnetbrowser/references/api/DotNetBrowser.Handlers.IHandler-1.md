# <a id="DotNetBrowser_Handlers_IHandler_1"></a> Interface IHandler<TParameters\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The common interface for all handlers that must be executed synchronously, but do not have to return a value.

```csharp
public interface IHandler<in TParameters>
```

#### Type Parameters

`TParameters` 

The handler parameters type.

## Methods

### <a id="DotNetBrowser_Handlers_IHandler_1_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback should be handled synchronously.
In a number of cases, the Chromium engine will be blocked until this method returns.

```csharp
void Handle(TParameters parameters)
```

#### Parameters

`parameters` TParameters

The handler parameters.

