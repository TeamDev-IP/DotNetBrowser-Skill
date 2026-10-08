# <a id="DotNetBrowser_Net_IHttpHeader"></a> Interface IHttpHeader

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Represents the single HTTP header with all its values.

```csharp
public interface IHttpHeader
```

## Properties

### <a id="DotNetBrowser_Net_IHttpHeader_Name"></a> Name

Gets the HTTP header name.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_IHttpHeader_Values"></a> Values

Gets the collection of the HTTP header values.

```csharp
IEnumerable<string> Values { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

