# <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters"></a> Class InterceptRequestParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the scheme handler.

```csharp
public sealed class InterceptRequestParameters : UrlRequestParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md) ← 
[InterceptRequestParameters](DotNetBrowser.Net.Handlers.InterceptRequestParameters.md)

#### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.UrlRequestParameters.md\#DotNetBrowser\_Net\_Handlers\_UrlRequestParameters\_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters_Headers"></a> Headers

Gets the collection of HTTP headers sent in the scope of the request.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)\>

### <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters_UploadData"></a> UploadData

Gets the data uploaded in the scope of the request.

```csharp
public IUploadData UploadData { get; }
```

#### Property Value

 [IUploadData](DotNetBrowser.Net.IUploadData.md)

