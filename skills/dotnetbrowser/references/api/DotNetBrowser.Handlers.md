# <a id="DotNetBrowser_Handlers"></a> Namespace DotNetBrowser.Handlers

### Classes

 [AsyncHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_AsyncHandler_2)

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

 [Handler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_2)

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

 [Handler<TParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_1)

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> interface.

### Interfaces

 [IHandler<TParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)

The common interface for all handlers that must be executed synchronously, but do not have to return a value.

 [IHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)

The common interface for all handlers.

## <a id="DotNetBrowser_Handlers_AsyncHandler_2"></a> Class AsyncHandler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class AsyncHandler<TParameters, TResponse> : IHandler<TParameters, TResponse>
```

##### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The result type.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AsyncHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_AsyncHandler_2)

##### Implements

[IHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Handlers_AsyncHandler_2__ctor_System_Func__0_System_Threading_Tasks_Task__1___"></a> AsyncHandler\(Func<TParameters, Task<TResponse\>\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.AsyncHandler%602" data-throw-if-not-resolved="false"></xref> class.

```csharp
public AsyncHandler(Func<TParameters, Task<TResponse>> func)
```

##### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.AsyncHandler%602.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

### Methods

#### <a id="DotNetBrowser_Handlers_AsyncHandler_2_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public TResponse Handle(TParameters parameters)
```

##### Parameters

`parameters` TParameters

The handler parameters.

##### Returns

 TResponse

An object that represents the response that should be
determined based on the provided parameters.

## <a id="DotNetBrowser_Handlers_Handler_2"></a> Class Handler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class Handler<TParameters, TResponse> : IHandler<TParameters, TResponse>
```

##### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The response type.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Handler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_2)

##### Implements

[IHandler<TParameters, TResponse\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Handlers_Handler_2__ctor_System_Func__0__1__"></a> Handler\(Func<TParameters, TResponse\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Handler(Func<TParameters, TResponse> func)
```

##### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, TResponse\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.Handler%602.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

### Methods

#### <a id="DotNetBrowser_Handlers_Handler_2_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public TResponse Handle(TParameters parameters)
```

##### Parameters

`parameters` TParameters

The handler parameters.

##### Returns

 TResponse

An object that represents the response that should be
determined based on the provided parameters.

### Operators

#### <a id="DotNetBrowser_Handlers_Handler_2_op_Implicit_System_Func__0__1___DotNetBrowser_Handlers_Handler__0__1_"></a> implicit operator Handler<TParameters, TResponse\>\(Func<TParameters, TResponse\>\)

The cast operator that can be used to cast <xref href="System.Func%602" data-throw-if-not-resolved="false"></xref> to <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref>

```csharp
public static implicit operator Handler<TParameters, TResponse>(Func<TParameters, TResponse> func)
```

##### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, TResponse\>

The <xref href="System.Func%602" data-throw-if-not-resolved="false"></xref> to cast from.

##### Returns

 [Handler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_2)<TParameters, TResponse\>

The corresponding <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

## <a id="DotNetBrowser_Handlers_Handler_1"></a> Class Handler<TParameters\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class Handler<TParameters> : IHandler<TParameters>
```

##### Type Parameters

`TParameters` 

The handler parameters type.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Handler<TParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_1)

##### Implements

[IHandler<TParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Handlers_Handler_1__ctor_System_Action__0__"></a> Handler\(Action<TParameters\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Handler(Action<TParameters> func)
```

##### Parameters

`func` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<TParameters\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.Handler%601.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

### Methods

#### <a id="DotNetBrowser_Handlers_Handler_1_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback should be handled synchronously.
In a number of cases, the Chromium engine will be blocked until this method returns.

```csharp
public void Handle(TParameters parameters)
```

##### Parameters

`parameters` TParameters

The handler parameters.

### Operators

#### <a id="DotNetBrowser_Handlers_Handler_1_op_Implicit_System_Action__0___DotNetBrowser_Handlers_Handler__0_"></a> implicit operator Handler<TParameters\>\(Action<TParameters\>\)

The cast operator that can be used to cast <xref href="System.Action%601" data-throw-if-not-resolved="false"></xref> to <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref>

```csharp
public static implicit operator Handler<TParameters>(Action<TParameters> value)
```

##### Parameters

`value` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<TParameters\>

The <xref href="System.Action%601" data-throw-if-not-resolved="false"></xref> to cast from.

##### Returns

 [Handler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_Handler_1)<TParameters\>

The corresponding <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

## <a id="DotNetBrowser_Handlers_IHandler_2"></a> Interface IHandler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The common interface for all handlers.

```csharp
public interface IHandler<in TParameters, out TResponse>
```

##### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The result type.

### Methods

#### <a id="DotNetBrowser_Handlers_IHandler_2_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
TResponse Handle(TParameters parameters)
```

##### Parameters

`parameters` TParameters

The handler parameters.

##### Returns

 TResponse

An object that represents the response that should be
determined based on the provided parameters.

## <a id="DotNetBrowser_Handlers_IHandler_1"></a> Interface IHandler<TParameters\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The common interface for all handlers that must be executed synchronously, but do not have to return a value.

```csharp
public interface IHandler<in TParameters>
```

##### Type Parameters

`TParameters` 

The handler parameters type.

### Methods

#### <a id="DotNetBrowser_Handlers_IHandler_1_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback should be handled synchronously.
In a number of cases, the Chromium engine will be blocked until this method returns.

```csharp
void Handle(TParameters parameters)
```

##### Parameters

`parameters` TParameters

The handler parameters.
