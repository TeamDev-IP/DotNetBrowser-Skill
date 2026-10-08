# <a id="DotNetBrowser_IAutoDisposable"></a> Interface IAutoDisposable

Namespace: [DotNetBrowser](DotNetBrowser.md)  
Assembly: DotNetBrowser.dll  

Represents the object which can be disposed by itself (without the explicit Dispose method call).

```csharp
public interface IAutoDisposable
```

## Properties

### <a id="DotNetBrowser_IAutoDisposable_IsDisposed"></a> IsDisposed

Indicates if the object is already disposed.

```csharp
bool IsDisposed { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_IAutoDisposable_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
event EventHandler Disposed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler)

