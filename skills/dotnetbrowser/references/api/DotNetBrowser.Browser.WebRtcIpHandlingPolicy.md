# <a id="DotNetBrowser_Browser_WebRtcIpHandlingPolicy"></a> Enum WebRtcIpHandlingPolicy

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The media performance/privacy tradeoffs which affect how WebRTC traffic will be routed and
how much local address information will be exposed.

```csharp
public enum WebRtcIpHandlingPolicy
```

## Fields

`Default = 1` 

This is the default behavior. Currently, WebRTC has the right to enumerate
all interfaces and bind them to discover public interfaces.



`DefaultPublicAndPrivateInterfaces = 3` 

WebRTC should only use the default route used by HTTP. This also exposes the
associated default private address. Default route is the route chosen by the
OS on a multi-homed endpoint.



`DefaultPublicInterfacesOnly = 2` 

WebRTC should only use the default route used by HTTP. This doesn't expose
any local addresses.



`DisableNonProxiedUdp = 4` 

WebRTC should only use TCP to contact peers or servers unless the proxy
server supports UDP. This doesn't expose any local addresses either.



