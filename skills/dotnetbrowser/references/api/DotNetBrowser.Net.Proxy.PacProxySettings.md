# <a id="DotNetBrowser_Net_Proxy_PacProxySettings"></a> Class PacProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

With this proxy configuration the connection uses proxy settings
received from proxy auto-config (PAC) file which is located at
the specific address.

<p></p>

In case PAC script fails, a direct connection will be used.

```csharp
public sealed class PacProxySettings : ProxySettings
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.ProxySettings.md) ← 
[PacProxySettings](DotNetBrowser.Net.Proxy.PacProxySettings.md)

#### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.ProxySettings.md\#DotNetBrowser\_Net\_Proxy\_ProxySettings\_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_Proxy_PacProxySettings__ctor_System_String_"></a> PacProxySettings\(string\)

Constructs a new PacProxySettings instance initiated with
the pacUrl URL address where PAC file with
proxy settings is located. The address of the PAC file must be a
valid URL address. The address can contain a path to the PAC
file on local file system.

```csharp
public PacProxySettings(string pacUrl)
```

#### Parameters

`pacUrl` [string](https://learn.microsoft.com/dotnet/api/system.string)

URL address of the PAC file with proxy settings.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when <code class="paramref">pacUrl</code> is null, empty or contain only white space.

## Properties

### <a id="DotNetBrowser_Net_Proxy_PacProxySettings_PacUrl"></a> PacUrl

The URL address of the PAC file with proxy settings.

```csharp
public string PacUrl { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

