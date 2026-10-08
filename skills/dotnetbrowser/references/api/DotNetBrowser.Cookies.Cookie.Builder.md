# <a id="DotNetBrowser_Cookies_Cookie_Builder"></a> Class Cookie.Builder

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct cookie.

```csharp
public class Cookie.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Cookie.Builder](DotNetBrowser.Cookies.Cookie.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

## Constructors

### <a id="DotNetBrowser_Cookies_Cookie_Builder__ctor_System_String_"></a> Builder\(string\)

Creates a new <xref href="DotNetBrowser.Cookies.Cookie" data-throw-if-not-resolved="false"></xref> builder.

```csharp
public Builder(string domainName)
```

#### Parameters

`domainName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the domain this cookie belongs too. Please note, that the domain is also required for cookies with
<code>__Host</code> prefix.

## Properties

### <a id="DotNetBrowser_Cookies_Cookie_Builder_CreationTime"></a> CreationTime

Gets or sets cookie creation time.

```csharp
public DateTime CreationTime { get; set; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

### <a id="DotNetBrowser_Cookies_Cookie_Builder_DomainName"></a> DomainName

Gets the domain name for this cookie.

```csharp
public string DomainName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cookies_Cookie_Builder_ExpirationTime"></a> ExpirationTime

Gets or sets cookie expiration time.

```csharp
public DateTime? ExpirationTime { get; set; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

### <a id="DotNetBrowser_Cookies_Cookie_Builder_HttpOnly"></a> HttpOnly

Gets or sets the <i>HttpOnly</i> attribute.
The <code>HttpOnly</code> cookie attribute can help to mitigate hijacking and XSS attacks
by preventing access to cookie value through JavaScript.

```csharp
public bool HttpOnly { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cookies_Cookie_Builder_Name"></a> Name

Gets or sets the name of the cookie.

```csharp
public string Name { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

### <a id="DotNetBrowser_Cookies_Cookie_Builder_Path"></a> Path

Gets or sets the path on the server to which the browser returns this cookie. The
cookie is visible to all sub-paths on the server.

```csharp
public string Path { get; set; }
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

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

### <a id="DotNetBrowser_Cookies_Cookie_Builder_SameSite"></a> SameSite

Gets or sets the <code>SameSite</code> attribute value of the cookie.
This attribute denotes if your cookie should be restricted to a first-party or same-site context.

```csharp
public SameSite SameSite { get; set; }
```

#### Property Value

 [SameSite](DotNetBrowser.Cookies.SameSite.md)

#### Remarks

<p>
    By default, the attribute value is set to <xref href="DotNetBrowser.Cookies.SameSite.LaxMode" data-throw-if-not-resolved="false"></xref> which means
    cookies are only set when the domain in the URL of the browser matches the domain of the
    cookie — a first-party cookie.
</p>
<p>
    The <xref href="DotNetBrowser.Cookies.SameSite.None" data-throw-if-not-resolved="false"></xref> value requires that the <xref href="DotNetBrowser.Cookies.Cookie.Builder.Secure" data-throw-if-not-resolved="false"></xref>
    attribute
    is set to <code>true</code>.
</p>

### <a id="DotNetBrowser_Cookies_Cookie_Builder_Secure"></a> Secure

Gets or sets the <code>Secure</code> attribute value of the cookie.
A secure cookie is only sent to the server with an encrypted
request over the HTTPS protocol.

```csharp
public bool Secure { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cookies_Cookie_Builder_Value"></a> Value

Gets or sets the value of the cookie.

```csharp
public string Value { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

## Methods

### <a id="DotNetBrowser_Cookies_Cookie_Builder_Build"></a> Build\(\)

Builds an HTTP cookie.

```csharp
public Cookie Build()
```

#### Returns

 [Cookie](DotNetBrowser.Cookies.Cookie.md)

The constructed <xref href="DotNetBrowser.Cookies.Cookie" data-throw-if-not-resolved="false"></xref> instance.

