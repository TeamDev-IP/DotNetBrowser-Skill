# <a id="DotNetBrowser_IAutoDisposable_1"></a> Interface IAutoDisposable<TArgs\>

Namespace: [DotNetBrowser](DotNetBrowser.md)  
Assembly: DotNetBrowser.dll  

Represents the object which can be disposed by itself (without the explicit Dispose method call).

```csharp
public interface IAutoDisposable<TArgs> : IAutoDisposable
```

#### Type Parameters

`TArgs` 

The type of the event arguments for the <xref href="DotNetBrowser.IAutoDisposable%601.Disposed" data-throw-if-not-resolved="false"></xref>
event.

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

### <a id="DotNetBrowser_IAutoDisposable_1_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
event EventHandler<TArgs> Disposed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<TArgs\>

