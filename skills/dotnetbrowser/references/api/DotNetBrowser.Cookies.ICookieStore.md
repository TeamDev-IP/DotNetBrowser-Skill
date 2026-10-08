# <a id="DotNetBrowser_Cookies_ICookieStore"></a> Interface ICookieStore

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

The system for storing and retrieving cookies. The cookies can be stored in
the process memory (session cookies) or in files (persistent cookies).
The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> instance provides access to both session and persistent cookies.

```csharp
public interface ICookieStore : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

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

## Properties

### <a id="DotNetBrowser_Cookies_ICookieStore_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Cookies_ICookieStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Cookies_ICookieStore_Delete_DotNetBrowser_Cookies_Cookie_"></a> Delete\(Cookie\)

Deletes one specific cookie. The cookie instance can be received from
a list of cookies returned from the <xref href="DotNetBrowser.Cookies.ICookieStore.GetAllCookies(System.String)" data-throw-if-not-resolved="false"></xref> method.

```csharp
Task Delete(Cookie cookie)
```

#### Parameters

`cookie` [Cookie](DotNetBrowser.Cookies.Cookie.md)

cookie to delete.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the cookie was deleted.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Cookies_ICookieStore_DeleteAllCookies"></a> DeleteAllCookies\(\)

Deletes all of the cookies including session, secure or HTTP only cookies.

```csharp
Task<int> DeleteAllCookies()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of deleted cookies.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Cookies_ICookieStore_Flush"></a> Flush\(\)

Use this method to save all the changes you apply to this cookie storage.
By default all the changes to the cookie store are made in memory, so when
you restart the application you will not see the changes you made if you
don't invoke this method on application exit. You can invoke this method
after every change you made to cookie storage.

```csharp
void Flush()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Cookies_ICookieStore_GetAllCookies_System_String_"></a> GetAllCookies\(string\)

Returns all the cookies for given url including HTTP only cookies.

```csharp
Task<IEnumerable<Cookie>> GetAllCookies(string url = null)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL associated with the returned cookies.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Cookie](DotNetBrowser.Cookies.Cookie.md)\>\>

The collection of all the cookies or an empty collection when there's no cookies.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Cookies_ICookieStore_SetCookie_DotNetBrowser_Cookies_Cookie_"></a> SetCookie\(Cookie\)

Sets a session cookie given explicit user-provided cookie attributes.

```csharp
Task<bool> SetCookie(Cookie cookie)
```

#### Parameters

`cookie` [Cookie](DotNetBrowser.Cookies.Cookie.md)

An HTTP cookie.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

<code>true</code> when session cookie was inserted successfully, <code>false</code> otherwise.

#### Remarks

If you set the cookie successfully and the method returns <code>true</code> and you
decide to find the cookie in the list of all cookies, please note that
the cookie storage can modify some cookies attributes, such as domain or expiration time.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cookie</code> is null or the cookie cannot be set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

