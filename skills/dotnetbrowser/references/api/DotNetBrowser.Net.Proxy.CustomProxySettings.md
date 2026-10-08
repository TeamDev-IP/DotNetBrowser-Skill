# <a id="DotNetBrowser_Net_Proxy_CustomProxySettings"></a> Class CustomProxySettings

Namespace: [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)  
Assembly: DotNetBrowser.dll  

Describes a user's proxy settings.

```csharp
public sealed class CustomProxySettings : ProxySettings
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProxySettings](DotNetBrowser.Net.Proxy.ProxySettings.md) ← 
[CustomProxySettings](DotNetBrowser.Net.Proxy.CustomProxySettings.md)

#### Inherited Members

[ProxySettings.Type](DotNetBrowser.Net.Proxy.ProxySettings.md\#DotNetBrowser\_Net\_Proxy\_ProxySettings\_Type), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings__ctor_System_String_System_String_"></a> CustomProxySettings\(string, string\)

Constructs a new CustomProxySettings instance with given proxy rules.

```csharp
public CustomProxySettings(string rules, string exceptions = "")
```

#### Parameters

`rules` [string](https://learn.microsoft.com/dotnet/api/system.string)

string that represents proxy rules in specified format. The string should be a
semicolon-separated list of ordered proxies that apply to a particular URL scheme.

`exceptions` [string](https://learn.microsoft.com/dotnet/api/system.string)

string that represents the set of URLs that should bypass the proxy settings.

#### Remarks

Examples of the proxy rules string:
<li>
    <code>"http=foopy:80;ftp=foopy2"</code>use HTTP proxy "foopy:80" for <code>http://</code> URLs,
    and HTTP proxy "foopy2:80" for <code>%ftp://</code> URLs.
</li>
<li><code>"socks4://foopy"</code>use SOCKS v4 proxy "foopy:1080" for all URLs.</li>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when <code class="paramref">rules</code> is null, empty or contain only white space.

## Properties

### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings_Exceptions"></a> Exceptions

The set of URLs that should bypass the proxy settings.

```csharp
public string Exceptions { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

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

### <a id="DotNetBrowser_Net_Proxy_CustomProxySettings_Rules"></a> Rules

The proxy rules in specified format. The string should be a
semicolon-separated list of ordered proxies that apply to a particular URL scheme.

```csharp
public string Rules { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

Examples of the proxyRules string:
<li>
    <code>"http=foopy:80;ftp=foopy2"</code> - use HTTP proxy "foopy:80" for <code>http://</code> URLs,
    and HTTP proxy "foopy2:80" for <code>%ftp://</code> URLs.
</li>
<li><code>"foopy:80"</code> - use HTTP proxy "foopy:80" for all URLs.</li>
<li><code>"socks4://foopy"</code> - use SOCKS v4 proxy "foopy:1080" for all URLs.</li>

