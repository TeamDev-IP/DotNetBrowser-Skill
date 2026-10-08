# <a id="DotNetBrowser_Handlers_Handler_1"></a> Class Handler<TParameters\>

Namespace: [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public sealed class Handler<TParameters> : IHandler<TParameters>
```

#### Type Parameters

`TParameters` 

The handler parameters type.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Handler<TParameters\>](DotNetBrowser.Handlers.Handler\-1.md)

#### Implements

[IHandler<TParameters\>](DotNetBrowser.Handlers.IHandler\-1.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Handlers_Handler_1__ctor_System_Action__0__"></a> Handler\(Action<TParameters\>\)

Initializes an instance of the <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Handler(Action<TParameters> func)
```

#### Parameters

`func` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<TParameters\>

The function that must be executed when the <xref href="DotNetBrowser.Handlers.Handler%601.Handle(%600)" data-throw-if-not-resolved="false"></xref> method is called.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">func</code> is null.

## Methods

### <a id="DotNetBrowser_Handlers_Handler_1_Handle__0_"></a> Handle\(TParameters\)

This method is called when the Chromium callback should be handled synchronously.
In a number of cases, the Chromium engine will be blocked until this method returns.

```csharp
public void Handle(TParameters parameters)
```

#### Parameters

`parameters` TParameters

The handler parameters.

## Operators

### <a id="DotNetBrowser_Handlers_Handler_1_op_Implicit_System_Action__0___DotNetBrowser_Handlers_Handler__0_"></a> implicit operator Handler<TParameters\>\(Action<TParameters\>\)

The cast operator that can be used to cast <xref href="System.Action%601" data-throw-if-not-resolved="false"></xref> to <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref>

```csharp
public static implicit operator Handler<TParameters>(Action<TParameters> value)
```

#### Parameters

`value` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<TParameters\>

The <xref href="System.Action%601" data-throw-if-not-resolved="false"></xref> to cast from.

#### Returns

 [Handler](DotNetBrowser.Handlers.Handler\-1.md)<TParameters\>

The corresponding <xref href="DotNetBrowser.Handlers.Handler%601" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

