# <a id="DotNetBrowser_Cookies"></a> Namespace DotNetBrowser.Cookies

### Classes

 [Cookie.Builder](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie_Builder)

A builder class to construct cookie.

 [Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

Represents an HTTP cookie.

### Interfaces

 [ICookieStore](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_ICookieStore)

The system for storing and retrieving cookies. The cookies can be stored in
the process memory (session cookies) or in files (persistent cookies).
The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> instance provides access to both session and persistent cookies.

### Enums

 [SameSite](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_SameSite)

The SameSite cookie attribute values of the <code>Set-Cookie</code> HTTP response header. This attribute is used to
declare in which context the cookies can be sent.

## <a id="DotNetBrowser_Cookies_Cookie"></a> Class Cookie

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

Represents an HTTP cookie.

```csharp
public sealed class Cookie
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cookies_Cookie_CreationTime"></a> CreationTime

Gets the cookie creation time.

```csharp
public DateTime CreationTime { get; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

#### <a id="DotNetBrowser_Cookies_Cookie_DomainName"></a> DomainName

Gets the domain name set for this cookie. It specifies allowed hosts
to receive the cookie.

```csharp
public string DomainName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cookies_Cookie_ExpirationTime"></a> ExpirationTime

Gets the cookie expiration time.

```csharp
public DateTime? ExpirationTime { get; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

#### <a id="DotNetBrowser_Cookies_Cookie_IsHttpOnly"></a> IsHttpOnly

Gets the <code>HttpOnly</code> attribute value of the cookie.
The <code>HttpOnly</code> cookie attribute can help to mitigate hijacking and XSS attacks
by preventing access to cookie value through JavaScript.

```csharp
public bool IsHttpOnly { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cookies_Cookie_IsSecure"></a> IsSecure

Gets the <code>Secure</code> attribute value of the cookie.
A secure cookie is only sent to the server with an encrypted
request over the HTTPS protocol.

```csharp
public bool IsSecure { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cookies_Cookie_IsSession"></a> IsSession

Indicates whether this cookie is a session cookie without
expiration time.

```csharp
public bool IsSession { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cookies_Cookie_Name"></a> Name

Gets the name of the cookie.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cookies_Cookie_Path"></a> Path

Gets the path on the server to which the browser returns this cookie. The
cookie is visible to all sub-paths on the server.

```csharp
public string Path { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

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

#### <a id="DotNetBrowser_Cookies_Cookie_SameSite"></a> SameSite

Gets the <code>SameSite</code> attribute value of the cookie.
This attribute denotes if your cookie is restricted to a first-party or same-site context.

```csharp
public SameSite SameSite { get; }
```

##### Property Value

 [SameSite](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_SameSite)

##### Remarks

<p>
    By default, the attribute value is set to <xref href="DotNetBrowser.Cookies.SameSite.LaxMode" data-throw-if-not-resolved="false"></xref> which means
    cookies are only set when the domain in the URL of the browser matches the domain of the
    cookie — a first-party cookie.
</p>

#### <a id="DotNetBrowser_Cookies_Cookie_Value"></a> Value

Gets the value of the cookie.

```csharp
public string Value { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Cookies_Cookie_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Cookies_Cookie_Builder"></a> Class Cookie.Builder

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct cookie.

```csharp
public class Cookie.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Cookie.Builder](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

### Constructors

#### <a id="DotNetBrowser_Cookies_Cookie_Builder__ctor_System_String_"></a> Builder\(string\)

Creates a new <xref href="DotNetBrowser.Cookies.Cookie" data-throw-if-not-resolved="false"></xref> builder.

```csharp
public Builder(string domainName)
```

##### Parameters

`domainName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the domain this cookie belongs too. Please note, that the domain is also required for cookies with
<code>__Host</code> prefix.

### Properties

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_CreationTime"></a> CreationTime

Gets or sets cookie creation time.

```csharp
public DateTime CreationTime { get; set; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_DomainName"></a> DomainName

Gets the domain name for this cookie.

```csharp
public string DomainName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_ExpirationTime"></a> ExpirationTime

Gets or sets cookie expiration time.

```csharp
public DateTime? ExpirationTime { get; set; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_HttpOnly"></a> HttpOnly

Gets or sets the <i>HttpOnly</i> attribute.
The <code>HttpOnly</code> cookie attribute can help to mitigate hijacking and XSS attacks
by preventing access to cookie value through JavaScript.

```csharp
public bool HttpOnly { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_Name"></a> Name

Gets or sets the name of the cookie.

```csharp
public string Name { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_Path"></a> Path

Gets or sets the path on the server to which the browser returns this cookie. The
cookie is visible to all sub-paths on the server.

```csharp
public string Path { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

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

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_SameSite"></a> SameSite

Gets or sets the <code>SameSite</code> attribute value of the cookie.
This attribute denotes if your cookie should be restricted to a first-party or same-site context.

```csharp
public SameSite SameSite { get; set; }
```

##### Property Value

 [SameSite](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_SameSite)

##### Remarks

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

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_Secure"></a> Secure

Gets or sets the <code>Secure</code> attribute value of the cookie.
A secure cookie is only sent to the server with an encrypted
request over the HTTPS protocol.

```csharp
public bool Secure { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_Value"></a> Value

Gets or sets the value of the cookie.

```csharp
public string Value { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty or blank.

### Methods

#### <a id="DotNetBrowser_Cookies_Cookie_Builder_Build"></a> Build\(\)

Builds an HTTP cookie.

```csharp
public Cookie Build()
```

##### Returns

 [Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

The constructed <xref href="DotNetBrowser.Cookies.Cookie" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Cookies_ICookieStore"></a> Interface ICookieStore

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

The system for storing and retrieving cookies. The cookies can be stored in
the process memory (session cookies) or in files (persistent cookies).
The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> instance provides access to both session and persistent cookies.

```csharp
public interface ICookieStore : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

<p>
    The persistent cookies are stored in the Browser cache directory.
</p>
<p>
    So, if Browser A and B have the same cache directory, then they will access
    the cookies of each other.
</p>
<p>
    If you need to configure each Browser to use unique cookie storage which is
    not accessible for other Browser instances, you need to provide unique
    user data directory for each Browser instance. The user data directory path
    can be provided via configured <xref href="DotNetBrowser.Engine.EngineOptions.UserDataDirectory" data-throw-if-not-resolved="false"></xref> object that
    must be passed into the <code>EngineFactory.Create</code> method.
</p>

### Properties

#### <a id="DotNetBrowser_Cookies_ICookieStore_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Cookies_ICookieStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

### Methods

#### <a id="DotNetBrowser_Cookies_ICookieStore_Delete_DotNetBrowser_Cookies_Cookie_"></a> Delete\(Cookie\)

Deletes one specific cookie. The cookie instance can be received from
a list of cookies returned from the <xref href="DotNetBrowser.Cookies.ICookieStore.GetAllCookies(System.String)" data-throw-if-not-resolved="false"></xref> method.

```csharp
Task Delete(Cookie cookie)
```

##### Parameters

`cookie` [Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

cookie to delete.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the cookie was deleted.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Cookies_ICookieStore_DeleteAllCookies"></a> DeleteAllCookies\(\)

Deletes all of the cookies including session, secure or HTTP only cookies.

```csharp
Task<int> DeleteAllCookies()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of deleted cookies.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Cookies_ICookieStore_Flush"></a> Flush\(\)

Use this method to save all the changes you apply to this cookie storage.
By default all the changes to the cookie store are made in memory, so when
you restart the application you will not see the changes you made if you
don't invoke this method on application exit. You can invoke this method
after every change you made to cookie storage.

```csharp
void Flush()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Cookies_ICookieStore_GetAllCookies_System_String_"></a> GetAllCookies\(string\)

Returns all the cookies for given url including HTTP only cookies.

```csharp
Task<IEnumerable<Cookie>> GetAllCookies(string url = null)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL associated with the returned cookies.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)\>\>

The collection of all the cookies or an empty collection when there's no cookies.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Cookies_ICookieStore_SetCookie_DotNetBrowser_Cookies_Cookie_"></a> SetCookie\(Cookie\)

Sets a session cookie given explicit user-provided cookie attributes.

```csharp
Task<bool> SetCookie(Cookie cookie)
```

##### Parameters

`cookie` [Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

An HTTP cookie.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

<code>true</code> when session cookie was inserted successfully, <code>false</code> otherwise.

##### Remarks

If you set the cookie successfully and the method returns <code>true</code> and you
decide to find the cookie in the list of all cookies, please note that
the cookie storage can modify some cookies attributes, such as domain or expiration time.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cookie</code> is null or the cookie cannot be set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Cookies_SameSite"></a> Enum SameSite

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

The SameSite cookie attribute values of the <code>Set-Cookie</code> HTTP response header. This attribute is used to
declare in which context the cookies can be sent.

```csharp
public enum SameSite
```

### Fields

`LaxMode = 2` 

The cookie can be sent with top-level navigations from a third-party site to the web site with the domain matching
the cookie. This is the default value in modern browsers.



`None = 3` 

The cookie can be sent in a third-party context. To use this mode the cookie must also be marked as secure.



`StrictMode = 1` 

The cookie can only be sent in a first-party context, when the cookie matches the domain of the current site.
