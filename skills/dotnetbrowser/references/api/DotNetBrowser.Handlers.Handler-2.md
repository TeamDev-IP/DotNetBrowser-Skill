# <a id="DotNetBrowser_Handlers_Handler_2"></a> Class Handler<TParameters, TResponse\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%602" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class Handler<TParameters, TResponse> : IHandler<TParameters, TResponse>
```

#### Type Parameters

`TParameters` 

The handler parameters type.

`TResponse` 

The response type.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Handler<TParameters, TResponse\>](DotNetBrowser.Handlers.Handler\-2.md)

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

### <a id="DotNetBrowser_Handlers_Handler_2__ctor_System_Func__0__1__"></a> Handler\(Func<TParameters, TResponse\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Handler(Func<TParameters, TResponse> func)
```

#### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, TResponse\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.Handler%602.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

## Methods

### <a id="DotNetBrowser_Handlers_Handler_2_Handle__0_"></a> Handle\(TParameters\)

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

## Operators

### <a id="DotNetBrowser_Handlers_Handler_2_op_Implicit_System_Func__0__1___DotNetBrowser_Handlers_Handler__0__1_"></a> implicit operator Handler<TParameters, TResponse\>\(Func<TParameters, TResponse\>\)

The cast operator that can be used to cast <xref href="System.Func%602" data-throw-if-not-resolved="false"></xref> to <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref>

```csharp
public static implicit operator Handler<TParameters, TResponse>(Func<TParameters, TResponse> func)
```

#### Parameters

`func` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TParameters, TResponse\>

The <xref href="System.Func%602" data-throw-if-not-resolved="false"></xref> to cast from.

#### Returns

 [Handler](DotNetBrowser.Handlers.Handler\-2.md)<TParameters, TResponse\>

The corresponding <xref href="DotNetBrowser.Handlers.Handler%602" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

