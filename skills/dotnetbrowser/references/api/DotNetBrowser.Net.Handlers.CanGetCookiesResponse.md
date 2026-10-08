# <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse"></a> Class CanGetCookiesResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanGetCookiesResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanGetCookiesResponse](DotNetBrowser.Net.Handlers.CanGetCookiesResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse_Allow"></a> Allow\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that
allows sending cookies back to web server.

```csharp
public static CanGetCookiesResponse Allow()
```

#### Returns

 [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.CanGetCookiesResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that
denies sending cookies back to web server.

```csharp
public static CanGetCookiesResponse Deny()
```

#### Returns

 [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.CanGetCookiesResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref> implementation.

