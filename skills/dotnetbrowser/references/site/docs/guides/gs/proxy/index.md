
# Proxy

**Lead**
This document describes how proxy functionality works in DotNetBrowser, namely how to configure proxy settings and handle proxy authentication requests.


**Note**
DotNetBrowser uses system proxy settings by default.


## System proxy

DotNetBrowser uses the same settings as Microsoft Internet Explorer.

## Configurations

If you do not want to use the system proxy settings, you can configure each `Profile` with its own proxy settings using `Proxy`:


**C#**
```csharp
IProxy proxy = profile.Proxy;
```

**VB**
```vb
Dim proxy As IProxy = profile.Proxy
```



If you use `engine.Profiles.Default.Proxy`, you get the `Proxy` instance associated with the default profile.

If you want to tell the library to use the system proxy settings again, call:


**C#**
```csharp
engine.Profiles.Default.Proxy.Settings = new SystemProxySettings();
```

**VB**
```vb
engine.Profiles.Default.Proxy.Settings = New SystemProxySettings()
```



**Note**
Proxy settings are stored in the [User Data](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory) directory. If you configure Engine to use specific User Data directory, then the proxy settings will be saved and restored the next time you create it.


### Direct

The connection does not use proxy server at all in this configuration:


**C#**
```csharp
engine.Profiles.Default.Proxy.Settings = new DirectProxySettings();
```

**VB**
```vb
engine.Profiles.Default.Proxy.Settings = New DirectProxySettings()
```



### Auto detect

Proxy settings are automatically detected in this configuration:


**C#**
```csharp
engine.Profiles.Default.Proxy.Settings = new AutoDetectProxySettings();
```

**VB**
```vb
engine.Profiles.Default.Proxy.Settings = New AutoDetectProxySettings()
```



### Custom proxy settings

You can provide custom proxy settings for HTTP, HTTPS, and FTP protocols:


**C#**
```csharp
string proxyRules = "http=foo:80;https=foo:80;ftp=foo:80;socks=foo:80";
string exceptions = "<local>";  // bypass proxy server for local web pages.
engine.Profiles.Default.Proxy.Settings = new CustomProxySettings(proxyRules, exceptions);
```

**VB**
```vb
Dim proxyRules As String = "http=foo:80;https=foo:80;ftp=foo:80;socks=foo:80"
Dim exceptions As String = "<local>" ' bypass proxy server for local web pages.
engine.Profiles.Default.Proxy.Settings = New CustomProxySettings(proxyRules, exceptions)
```



**Note**
The IP address of proxy server is also acceptable in the rules. For example, `http=127.0.0.1:80`.


Examples of the proxy rules:

- `http=foopy:80;ftp=foopy2` means HTTP proxy `foopy:80` for `http://` URLs and HTTP proxy `foopy2:80` for `ftp://` URLs;
- `foopy:80` means HTTP proxy `foopy:80` for all URLs;
- `socks4://foopy` means SOCKS v4 proxy `foopy:1080` for all URLs.

The format of the exceptions can be as follows:

- `[ URL_SCHEME "://" ] HOSTNAME_PATTERN [ ":" <port> ]`

    Examples:

    ```
    foobar.com
    *foobar.com
    *.foobar.com
    *foobar.com:99
    https://x.*.y.com:99
    ```

- `"." HOSTNAME_SUFFIX_PATTERN [ ":" PORT ]`

    Examples:

    ```
    .google.com
    .com
    http://.google.com
    ```

- `[ SCHEME "://" ] IP_LITERAL [ ":" PORT ]`

    Examples:

    ```
    127.0.1
    [0:0::1]
    [::1]
    http://[::1]:99
    ```

- `IP_LITERAL "/" PREFIX_LENGTH_IN_BITS`.

    Examples:

    ```
    192.168.1.1/16
    fefe:13::abc/33
    ```

- `"<local>"`. Match local addresses. `<local>` means that the host matches `127.0.0.1`, `::1`, and `localhost`.

If you need to provide several exception rules, you can separate them by comma, for example: `*foobar.com,.google.com,<local>`.

### PAC

Proxy settings are received from the proxy auto-config (PAC) file. You must provide a valid URL to the required PAC file:


**C#**
```csharp
engine.Profiles.Default.Proxy.Settings = new PacProxySettings("<pac-file-url>");
```

**VB**
```vb
engine.Profiles.Default.Proxy.Settings = New PacProxySettings("<pac-file-url>")
```



**Note**
PAC file URL must be a valid `http://` address. You cannot provide a path to a `*.pac` file stored on a local file system. The name of the PAC file must have the _pac_ extension, for example, `http://my-site.com/proxy.pac`. The pac file must be served with the `application/x-ns-proxy-autoconfig` mime type on a web server .


Refer to the [PAC Script Error](https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#pac-script-error) section for details.

## Authentication

DotNetBrowser supports proxy authentication. Refer to the [Authentication](https://teamdev.com/dotnetbrowser/docs/guides/gs/authentication/#proxy-basic-digest-and-ntlm-authentication) section for details.

## Multiple proxies
To use multiple proxy servers in the same .NET application, create a separate `IProfile` instance for each proxy. All `IBrowser` instances bound to the same `IProfile` will share the proxy settings.
