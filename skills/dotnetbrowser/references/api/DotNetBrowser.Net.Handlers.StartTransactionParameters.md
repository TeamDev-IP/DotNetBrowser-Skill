# <a id="DotNetBrowser_Net_Handlers_StartTransactionParameters"></a> Class StartTransactionParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartTransactionParameters : UrlRequestParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md) ← 
[StartTransactionParameters](DotNetBrowser.Net.Handlers.StartTransactionParameters.md)

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

### <a id="DotNetBrowser_Net_Handlers_StartTransactionParameters_Headers"></a> Headers

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)\>

