# <a id="DotNetBrowser_Net_Proxy_IProxy"></a> Interface IProxy

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

The service that allows modifying the proxy configuration for the current engine.

```csharp
public interface IProxy : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Net_Proxy_IProxy_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Net_Proxy_IProxy_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Net_Proxy_IProxy_Settings"></a> Settings

Gets or sets the current proxy settings.

```csharp
ProxySettings Settings { get; set; }
```

#### Property Value

 [ProxySettings](DotNetBrowser.Net.Proxy.ProxySettings.md)

