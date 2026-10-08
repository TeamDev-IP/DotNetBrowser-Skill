# <a id="DotNetBrowser_Cookies_Cookie"></a> Class Cookie

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

Represents an HTTP cookie.

```csharp
public sealed class Cookie
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Cookie](DotNetBrowser.Cookies.Cookie.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cookies_Cookie_CreationTime"></a> CreationTime

Gets the cookie creation time.

```csharp
public DateTime CreationTime { get; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

### <a id="DotNetBrowser_Cookies_Cookie_DomainName"></a> DomainName

Gets the domain name set for this cookie. It specifies allowed hosts
to receive the cookie.

```csharp
public string DomainName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cookies_Cookie_ExpirationTime"></a> ExpirationTime

Gets the cookie expiration time.

```csharp
public DateTime? ExpirationTime { get; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

### <a id="DotNetBrowser_Cookies_Cookie_IsHttpOnly"></a> IsHttpOnly

Gets the <code>HttpOnly</code> attribute value of the cookie.
The <code>HttpOnly</code> cookie attribute can help to mitigate hijacking and XSS attacks
by preventing access to cookie value through JavaScript.

```csharp
public bool IsHttpOnly { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cookies_Cookie_IsSecure"></a> IsSecure

Gets the <code>Secure</code> attribute value of the cookie.
A secure cookie is only sent to the server with an encrypted
request over the HTTPS protocol.

```csharp
public bool IsSecure { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cookies_Cookie_IsSession"></a> IsSession

Indicates whether this cookie is a session cookie without
expiration time.

```csharp
public bool IsSession { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cookies_Cookie_Name"></a> Name

Gets the name of the cookie.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cookies_Cookie_Path"></a> Path

Gets the path on the server to which the browser returns this cookie. The
cookie is visible to all sub-paths on the server.

```csharp
public string Path { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    <code>Path</code> indicates a URL path that must exist in the requested URL in order to send
    the <code>Cookie</code> header. The %x2F ("/") character is considered a directory separator,
    and subdirectories will match as well.
</p>
<p>
    For example, if <code>Path=/docs</code> is set, these paths will match:

<ul>
        <li>
            <code>/docs</code>
        </li>
        <li>
            <code>/docs/Web/</code>
        </li>
        <li>
            <code>/docs/Web/HTTP</code>
        </li>
    </ul>
</p>

### <a id="DotNetBrowser_Cookies_Cookie_SameSite"></a> SameSite

Gets the <code>SameSite</code> attribute value of the cookie.
This attribute denotes if your cookie is restricted to a first-party or same-site context.

```csharp
public SameSite SameSite { get; }
```

#### Property Value

 [SameSite](DotNetBrowser.Cookies.SameSite.md)

#### Remarks

<p>
    By default, the attribute value is set to <xref href="DotNetBrowser.Cookies.SameSite.LaxMode" data-throw-if-not-resolved="false"></xref> which means
    cookies are only set when the domain in the URL of the browser matches the domain of the
    cookie — a first-party cookie.
</p>

### <a id="DotNetBrowser_Cookies_Cookie_Value"></a> Value

Gets the value of the cookie.

```csharp
public string Value { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Cookies_Cookie_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

