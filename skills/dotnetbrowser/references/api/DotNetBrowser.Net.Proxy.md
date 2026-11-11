# <a id="DotNetBrowser_Net_Proxy"></a> Namespace DotNetBrowser.Net.Proxy

### Classes

 [AutoDetectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_AutoDetectProxySettings)

With this proxy configuration the connection automatically
detects proxy settings.

 [CustomProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_CustomProxySettings)

Describes a user's proxy settings.

 [DirectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_DirectProxySettings)

With this proxy configuration the connection doesn't use a proxy server.

 [PacProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_PacProxySettings)

With this proxy configuration the connection uses proxy settings
received from proxy auto-config (PAC) file which is located at
the specific address.

<p></p>

In case PAC script fails, a direct connection will be used.

 [ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings)

The base class for all proxy settings.

 [SystemProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_SystemProxySettings)

The system proxy settings defined by the operating system.

### Interfaces

 [IProxy](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_IProxy)

The service that allows modifying the proxy configuration for the current engine.

### Enums

 [ProxyType](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxyType)

Types of proxy settings.

## <a id="DotNetBrowser_Net_Proxy_AutoDetectProxySettings"></a> Class AutoDetectProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

With this proxy configuration the connection automatically
detects proxy settings.

```csharp
public sealed class AutoDetectProxySettings : ProxySettings
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings) ← 
[AutoDetectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_AutoDetectProxySettings)

##### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Net_Proxy_CustomProxySettings"></a> Class CustomProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

Describes a user's proxy settings.

```csharp
public sealed class CustomProxySettings : ProxySettings
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings) ← 
[CustomProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_CustomProxySettings)

##### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings__ctor_System_String_System_String_"></a> CustomProxySettings\(string, string\)

Constructs a new CustomProxySettings instance with given proxy rules.

```csharp
public CustomProxySettings(string rules, string exceptions = "")
```

##### Parameters

`rules` [string](https://learn.microsoft.com/dotnet/api/system.string)

string that represents proxy rules in specified format. The string should be a
semicolon-separated list of ordered proxies that apply to a particular URL scheme.

`exceptions` [string](https://learn.microsoft.com/dotnet/api/system.string)

string that represents the set of URLs that should bypass the proxy settings.

##### Remarks

Examples of the proxy rules string:
<li>
    <code>"http=foopy:80;ftp=foopy2"</code>use HTTP proxy "foopy:80" for <code>http://</code> URLs,
    and HTTP proxy "foopy2:80" for <code>%ftp://</code> URLs.
</li>
<li><code>"socks4://foopy"</code>use SOCKS v4 proxy "foopy:1080" for all URLs.</li>

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when <code class="paramref">rules</code> is null, empty or contain only white space.

### Properties

#### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings_Exceptions"></a> Exceptions

The set of URLs that should bypass the proxy settings.

```csharp
public string Exceptions { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

The format of the exceptions string can be any of the following:

<ul>
    <li>
        <code>[ URL_SCHEME "://" ] HOSTNAME_PATTERN [ ":" &lt;port&gt; ]</code>
        Examples:
        "foobar.com", "*foobar.com", "*.foobar.com", "*foobar.com:99", "https://x.*.y.com:99"
    </li>
    <li>
        <code>"." HOSTNAME_SUFFIX_PATTERN [ ":" PORT ]</code>
        Examples:
        ".google.com", ".com", "http://.google.com"
    </li>
    <li>
        <code>[ SCHEME "://" ] IP_LITERAL [ ":" PORT ]</code>
        Examples:
        "127.0.1", "[0:0::1]", "[::1]", "http://[::1]:99"
    </li>
    <li>
        <code>IP_LITERAL "/" PREFIX_LENGHT_IN_BITS</code>
        Examples:
        "192.168.1.1/16", "fefe:13::abc/33"
    </li>
    <li>
        <code>"&lt;local&gt;"</code>
        Match local addresses. The meaning of "&lt;local&gt;" is whether the host matches
        one of: "127.0.0.1", "::1", "localhost".
    </li>
</ul>
<p></p>

If you need to provide several exception rules you can separate them using comma:
"*foobar.com,.google.com,&lt;local&gt;".

#### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings_Rules"></a> Rules

The proxy rules in specified format. The string should be a
semicolon-separated list of ordered proxies that apply to a particular URL scheme.

```csharp
public string Rules { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

Examples of the proxyRules string:
<li>
    <code>"http=foopy:80;ftp=foopy2"</code> - use HTTP proxy "foopy:80" for <code>http://</code> URLs,
    and HTTP proxy "foopy2:80" for <code>%ftp://</code> URLs.
</li>
<li><code>"foopy:80"</code> - use HTTP proxy "foopy:80" for all URLs.</li>
<li><code>"socks4://foopy"</code> - use SOCKS v4 proxy "foopy:1080" for all URLs.</li>

## <a id="DotNetBrowser_Net_Proxy_DirectProxySettings"></a> Class DirectProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

With this proxy configuration the connection doesn't use a proxy server.

```csharp
public sealed class DirectProxySettings : ProxySettings
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings) ← 
[DirectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_DirectProxySettings)

##### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Net_Proxy_PacProxySettings"></a> Class PacProxySettings

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

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings) ← 
[PacProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_PacProxySettings)

##### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_Proxy_PacProxySettings__ctor_System_String_"></a> PacProxySettings\(string\)

Constructs a new PacProxySettings instance initiated with
the pacUrl URL address where PAC file with
proxy settings is located. The address of the PAC file must be a
valid URL address. The address can contain a path to the PAC
file on local file system.

```csharp
public PacProxySettings(string pacUrl)
```

##### Parameters

`pacUrl` [string](https://learn.microsoft.com/dotnet/api/system.string)

URL address of the PAC file with proxy settings.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when <code class="paramref">pacUrl</code> is null, empty or contain only white space.

### Properties

#### <a id="DotNetBrowser_Net_Proxy_PacProxySettings_PacUrl"></a> PacUrl

The URL address of the PAC file with proxy settings.

```csharp
public string PacUrl { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Proxy_ProxySettings"></a> Class ProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

The base class for all proxy settings.

```csharp
public abstract class ProxySettings
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings)

##### Derived

[AutoDetectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_AutoDetectProxySettings), 
[CustomProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_CustomProxySettings), 
[DirectProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_DirectProxySettings), 
[PacProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_PacProxySettings), 
[SystemProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_SystemProxySettings)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Proxy_ProxySettings_Type"></a> Type

Gets the type of proxy settings.

```csharp
public ProxyType Type { get; }
```

##### Property Value

 [ProxyType](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxyType)

## <a id="DotNetBrowser_Net_Proxy_SystemProxySettings"></a> Class SystemProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

The system proxy settings defined by the operating system.

```csharp
public sealed class SystemProxySettings : ProxySettings
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings) ← 
[SystemProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_SystemProxySettings)

##### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Net_Proxy_IProxy"></a> Interface IProxy

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

The service that allows modifying the proxy configuration for the current engine.

```csharp
public interface IProxy : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Net_Proxy_IProxy_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Net_Proxy_IProxy_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Net_Proxy_IProxy_Settings"></a> Settings

Gets or sets the current proxy settings.

```csharp
ProxySettings Settings { get; set; }
```

##### Property Value

 [ProxySettings](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_ProxySettings)

## <a id="DotNetBrowser_Net_Proxy_ProxyType"></a> Enum ProxyType

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

Types of proxy settings.

```csharp
public enum ProxyType
```

### Fields

`AutoDetect = 3` 

The automatically detected proxy settings.



`Custom = 5` 

The custom proxy settings.



`Direct = 2` 

The direct connection without proxy server.



`Pac = 4` 

The proxy settings obtained from the PAC file.



`System = 1` 

The proxy settings defined in operating system.
