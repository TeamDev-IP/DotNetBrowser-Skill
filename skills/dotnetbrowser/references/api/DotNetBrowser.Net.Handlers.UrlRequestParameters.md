# <a id="DotNetBrowser_Net_Handlers_UrlRequestParameters"></a> Class UrlRequestParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all the <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters containing
<xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UrlRequestParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md)

#### Derived

[InterceptRequestParameters](DotNetBrowser.Net.Handlers.InterceptRequestParameters.md), 
[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.ReceiveHeadersParameters.md), 
[SendUploadDataParameters](DotNetBrowser.Net.Handlers.SendUploadDataParameters.md), 
[SendUrlRequestParameters](DotNetBrowser.Net.Handlers.SendUrlRequestParameters.md), 
[StartTransactionParameters](DotNetBrowser.Net.Handlers.StartTransactionParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest"></a> UrlRequest

The URL request received from the Chromium engine.

```csharp
public UrlRequest UrlRequest { get; }
```

#### Property Value

 [UrlRequest](DotNetBrowser.Net.UrlRequest.md)

