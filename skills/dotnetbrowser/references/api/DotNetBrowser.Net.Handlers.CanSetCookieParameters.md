# <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters"></a> Class CanSetCookieParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanSetCookieParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[CanSetCookieParameters](DotNetBrowser.Net.Handlers.CanSetCookieParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters_Cookie"></a> Cookie

Gets the cookie received from the web server.

```csharp
public Cookie Cookie { get; }
```

#### Property Value

 [Cookie](DotNetBrowser.Cookies.Cookie.md)

### <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters_Url"></a> Url

Gets the URL associated with the cookie.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

