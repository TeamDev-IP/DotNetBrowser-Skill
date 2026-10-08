# <a id="DotNetBrowser_Net_Proxy"></a> Namespace DotNetBrowser.Net.Proxy

### Classes

 [AutoDetectProxySettings](DotNetBrowser.Net.Proxy.AutoDetectProxySettings.md)

With this proxy configuration the connection automatically
detects proxy settings.

 [CustomProxySettings](DotNetBrowser.Net.Proxy.CustomProxySettings.md)

Describes a user's proxy settings.

 [DirectProxySettings](DotNetBrowser.Net.Proxy.DirectProxySettings.md)

With this proxy configuration the connection doesn't use a proxy server.

 [PacProxySettings](DotNetBrowser.Net.Proxy.PacProxySettings.md)

With this proxy configuration the connection uses proxy settings
received from proxy auto-config (PAC) file which is located at
the specific address.

<p></p>

In case PAC script fails, a direct connection will be used.

 [ProxySettings](DotNetBrowser.Net.Proxy.ProxySettings.md)

The base class for all proxy settings.

 [SystemProxySettings](DotNetBrowser.Net.Proxy.SystemProxySettings.md)

The system proxy settings defined by the operating system.

### Interfaces

 [IProxy](DotNetBrowser.Net.Proxy.IProxy.md)

The service that allows modifying the proxy configuration for the current engine.

### Enums

 [ProxyType](DotNetBrowser.Net.Proxy.ProxyType.md)

Types of proxy settings.

