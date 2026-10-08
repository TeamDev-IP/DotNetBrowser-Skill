# <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters"></a> Class CanGetCookiesParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanGetCookiesParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.CanGetCookiesParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters_Cookies"></a> Cookies

Gets a collection of cookies that are going to be sent with the URL request.

```csharp
public IEnumerable<Cookie> Cookies { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Cookie](DotNetBrowser.Cookies.Cookie.md)\>

### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters_Url"></a> Url

Gets the URL associated with the cookies.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

