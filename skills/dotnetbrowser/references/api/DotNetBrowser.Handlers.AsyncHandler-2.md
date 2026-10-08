# <a id="DotNetBrowser_Handlers_AsyncHandler_2"></a> Class AsyncHandler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class AsyncHandler<TParameters, TResponse> : IHandler<TParameters, TResponse>
```

#### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The result type.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AsyncHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.AsyncHandler\-2.md)

#### Implements

[IHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.IHandler\-2.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Handlers_AsyncHandler_2__ctor_System_Func__0_System_Threading_Tasks_Task__1___"></a> AsyncHandler\(Func<TParameters, Task<TResponse\>\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.AsyncHandler%602" data-throw-if-not-resolved="false"></xref> class.

```csharp
public AsyncHandler(Func<TParameters, Task<TResponse>> func)
```

#### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.AsyncHandler%602.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

## Methods

### <a id="DotNetBrowser_Handlers_AsyncHandler_2_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public TResponse Handle(TParameters parameters)
```

#### Parameters

`parameters` TParameters

The handler parameters.

#### Returns

 TResponse

An object that represents the response that should be
determined based on the provided parameters.

