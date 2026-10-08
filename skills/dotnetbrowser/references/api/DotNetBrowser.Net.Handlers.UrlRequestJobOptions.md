# <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions"></a> Class UrlRequestJobOptions

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The options needed to create the <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UrlRequestJobOptions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJobOptions](DotNetBrowser.Net.Handlers.UrlRequestJobOptions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions_Headers"></a> Headers

Gets or sets the list of the HTTP headers that will be a part of the response.

```csharp
public List<HttpHeader> Headers { get; set; }
```

#### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[HttpHeader](DotNetBrowser.Net.HttpHeader.md)\>

### <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions_HttpStatusCode"></a> HttpStatusCode

Gets or sets the HTTP status code of the response.

```csharp
public HttpStatusCode HttpStatusCode { get; set; }
```

#### Property Value

 [HttpStatusCode](https://learn.microsoft.com/dotnet/api/system.net.httpstatuscode)

