# <a id="DotNetBrowser_Net_Handlers_NetworkParameters"></a> Class NetworkParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters.

```csharp
public class NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md)

#### Derived

[AuthenticateParameters](DotNetBrowser.Net.Handlers.AuthenticateParameters.md), 
[CanAccessFileParameters](DotNetBrowser.Net.Handlers.CanAccessFileParameters.md), 
[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.CanGetCookiesParameters.md), 
[CanSetCookieParameters](DotNetBrowser.Net.Handlers.CanSetCookieParameters.md), 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md), 
[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.VerifyCertificateParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_NetworkParameters_Network"></a> Network

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public INetwork Network { get; }
```

#### Property Value

 [INetwork](DotNetBrowser.Net.INetwork.md)

