# <a id="DotNetBrowser_Net_HttpHeader"></a> Class HttpHeader

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class HttpHeader : IHttpHeader
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HttpHeader](DotNetBrowser.Net.HttpHeader.md)

#### Implements

[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_HttpHeader__ctor_System_String_System_String___"></a> HttpHeader\(string, params string\[\]\)

Creates the HTTP header instance using its name and values collection.

```csharp
public HttpHeader(string name, params string[] values)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTTP header name

`values` [string](https://learn.microsoft.com/dotnet/api/system.string)\[\]

The collection of the HTTP header values

## Properties

### <a id="DotNetBrowser_Net_HttpHeader_Name"></a> Name

Gets the HTTP header name.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_HttpHeader_Values"></a> Values

Gets the collection of the HTTP header values.

```csharp
public IEnumerable<string> Values { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

