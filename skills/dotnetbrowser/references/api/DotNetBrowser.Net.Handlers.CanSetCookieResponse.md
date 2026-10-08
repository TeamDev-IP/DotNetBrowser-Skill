# <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse"></a> Class CanSetCookieResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class CanSetCookieResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanSetCookieResponse](DotNetBrowser.Net.Handlers.CanSetCookieResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse_Allow"></a> Allow\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> that allows saving the cookie.

```csharp
public static CanSetCookieResponse Allow()
```

#### Returns

 [CanSetCookieResponse](DotNetBrowser.Net.Handlers.CanSetCookieResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> that denies saving the cookie.

```csharp
public static CanSetCookieResponse Deny()
```

#### Returns

 [CanSetCookieResponse](DotNetBrowser.Net.Handlers.CanSetCookieResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref> implementation.

