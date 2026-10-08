# <a id="DotNetBrowser_Net_Proxy_ProxySettings"></a> Class ProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

The base class for all proxy settings.

```csharp
public abstract class ProxySettings
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.ProxySettings.md)

#### Derived

[AutoDetectProxySettings](DotNetBrowser.Net.Proxy.AutoDetectProxySettings.md), 
[CustomProxySettings](DotNetBrowser.Net.Proxy.CustomProxySettings.md), 
[DirectProxySettings](DotNetBrowser.Net.Proxy.DirectProxySettings.md), 
[PacProxySettings](DotNetBrowser.Net.Proxy.PacProxySettings.md), 
[SystemProxySettings](DotNetBrowser.Net.Proxy.SystemProxySettings.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Proxy_ProxySettings_Type"></a> Type

Gets the type of proxy settings.

```csharp
public ProxyType Type { get; }
```

#### Property Value

 [ProxyType](DotNetBrowser.Net.Proxy.ProxyType.md)

