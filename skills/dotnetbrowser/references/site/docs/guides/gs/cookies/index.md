
# Cookies

**Lead**
This document describes how to work with cookies.


## Overview

DotNetBrowser delegates the work with cookies to the Chromium engine. Chromium decides how to download cookies from a web server, extract them from the HTTP headers and store them in a local file system (persistent cookies) or in the memory (session cookies).

The `ICookieStore` interface allows you to get, modify, and remove cookies. The `Cookie` class provides information on a particular cookie.

To obtain the `ICookieStore` for a specific `Profile`, use the `Profile.CookieStore` property. To access the `CookieStore` associated with the default profile, use `engine.Profiles.Default.CookieStore`.

## Supported protocols

DotNetBrowser supports cookies that are sent using the following protocols:

- HTTP
- HTTPS
- WS (WebSocket)
- WSS (Secured WebSocket)

If a cookie is sent using a protocol that is not on the list, for example, `ftp://`, it will not be stored in the cookie storage.

## Working with cookies

DotNetBrowser supports the following kinds of cookies:

* **Persistent cookies** &mdash; stored in the Chromium user data directory. If you delete the Chromium user data directory, all the persistent cookies will be removed as well.
* **Session cookies** &mdash; stored in the application memory, and will be removed automatically when the application is terminated.
* **Secure cookies** &mdash; can only be transmitted over an encrypted connection which is HTTPS. This makes the cookie less likely to be exposed to cookie theft using eavesdropping.
* **HttpOnly cookies** &mdash; cannot be accessed by the client-side APIs, such as JavaScript. This restriction eliminates the threat of cookie theft using the [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) (XSS). However, the cookie remains vulnerable to [cross-site tracing](https://en.wikipedia.org/wiki/Cross-site_tracing) (XST) and [cross-site request forgery](https://en.wikipedia.org/wiki/Cross-site_request_forgery) (XSRF) attacks.

**Note**
When you modify cookies, use the `ICookieStore.Flush()` method to save the changes in the cookie store.


### Getting cookies

To get all cookies, use the `GetAllCookies()` method:


**C#**
```csharp
engine.Profiles.Default.CookieStore.GetAllCookies()
    .Result.ToList().ForEach(cookie => Console.WriteLine("cookie = " + cookie));
```

**VB**
```vb
engine.Profiles.Default.CookieStore.GetAllCookies().Result.ToList().
    ForEach(Sub(cookie) 
        Console.WriteLine("cookie = " & cookie.ToString())
    End Sub)
```



To get all cookies by a URL, use the `GetAllCookies()` method with a string parameter:


**C#**
```csharp
engine.Profiles.Default.CookieStore.GetAllCookies("https://www.google.com")
    .Result.ToList().ForEach(cookie => Console.WriteLine("cookie = " + cookie));
```

**VB**
```vb
engine.Profiles.Default.CookieStore.GetAllCookies("https://google.com").Result.ToList().
    ForEach(Sub(cookie)
        Console.WriteLine("cookie = " & cookie.ToString())
    End Sub)
```



### Creating cookies
#### Persistent

To create a persistent cookie, use the code sample below:


**C#**
```csharp
Cookie cookie = new Cookie.Builder("google.com")
{
    Name = "name",
    Value = "value",
    ExpirationTime = expirationTime,
    Path = "/"
}.Build();

bool success = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder("google.com") With {
    .Name = "name",
    .Value = "value",
    .ExpirationTime = expirationTime,
    .Path = "/"
}.Build()

Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



The code sample above creates a persistent cookie for the `http://www.google.com` URL. The `success` variable will be `true` if the cookie is created and added to the cookie storage successfully.

#### Session

To create a session cookie, use the code sample below:


**C#**
```csharp
Cookie cookie = new Cookie.Builder("google.com")
{
    Name = "name",
    Value = "value",
    Path = "/"
}.Build();

bool success = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder("google.com") With {
    .Name = "name",
    .Value = "value",
    .Path = "/"
}.Build()

Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



#### Cookies with specific prefixes

Some cookies with the particular names have a specific semantic.

Cookies with names starting with `__Host-` must be set with the secure flag, must be from a secure page (HTTPS), must not have a domain specified (and therefore aren't sent to subdomains) and the path must be `/`. The domain name should be specified via the API, but is used only for validation purposes in this case.


**C#**
```csharp
Cookie cookie = new Cookie.Builder("a.com")
{
    Name = "__Host-1PLSID",
    Value = "value",
    Secure = true,
    HttpOnly = false
}.Build();
bool success = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder("a.com") With {
    .Name = "__Host-1PLSID",
    .Value = "value",
    .Secure = True,
    .HttpOnly = False
}.Build()
Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



Cookies names starting with `__Secure-` (dash is part of the prefix) must be set with the secure flag from a secure page (HTTPS). Here is how to create these cookies:


**C#**
```csharp
Cookie cookie = new Cookie.Builder("a.com")
{
    Name = "__Secure-Asd",
    Path = "/",
    Secure = true
}.Build();
bool success = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder("a.com") With {
    .Name = "__Secure-Asd",
    .Path = "/",
    .Secure = True
}.Build()
Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



### Deleting cookies

To delete all cookies, use the `DeleteAllCookies()` method:


**C#**
```csharp
int numberOfDeletedCookies = engine.Profiles.Default.CookieStore.DeleteAllCookies().Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim numberOfDeletedCookies As Integer = 
        engine.Profiles.Default.CookieStore.DeleteAllCookies().Result
engine.Profiles.Default.CookieStore.Flush()
```



To delete one cookie, use the `Delete(Cookie)` method. The code sample below deletes all cookies one by one obtaining the result of the operation:


**C#**
```csharp
engine.Profiles.Default.CookieStore.GetAllCookies().Result.ToList().ForEach(c => 
    engine.Profiles.Default.CookieStore.Delete(c).Wait());
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
engine.Profiles.Default.CookieStore.GetAllCookies().Result.ToList().ForEach(Function(c) 
        engine.Profiles.Default.CookieStore.Delete(c).Wait()
    End Function)
engine.Profiles.Default.CookieStore.Flush()
```



### Suppressing cookies

You can control all incoming and outgoing cookies using the `CanSetCookieHandler` and `CanGetCookiesHandler` handlers of the `Network`.

To suppress the incoming cookies, use the code sample below:


**C#**
```csharp
network.CanSetCookieHandler = 
    new Handler<CanSetCookieParameters, CanSetCookieResponse>(p =>
    {
        return CanSetCookieResponse.Deny();
    });
```

**VB**
```vb
network.CanSetCookieHandler = 
    New Handler(Of CanSetCookieParameters, CanSetCookieResponse)(Function(p) 
        Return CanSetCookieResponse.Deny()
    End Function)
```



To suppress the outgoing cookies, use the code sample below:


**C#**
```csharp
network.CanGetCookiesHandler = 
    new Handler<CanGetCookiesParameters, CanGetCookiesResponse>(p =>
    {
        return CanGetCookiesResponse.Deny();
    });
```

**VB**
```vb
network.CanGetCookiesHandler = 
    New Handler(Of CanGetCookiesParameters, CanGetCookiesResponse)(Function(p)
        Return CanGetCookiesResponse.Deny()
    End Function)
```



## Third-party cookie control

You can configure how Chromium controls the third-party cookies:

* Turn the control off.
* Block third-party cookies.
* Block third-party cookies in incognito mode.

See available options in 
[CookieControlsMode](https://api.dotnetbrowser.dev/4.3.3/api/DotNetBrowser.Profile.CookieControlsMode)
enum.

For example:


**C#**
```csharp
IProfile profile = engine.Profiles.Default;
profile.Preferences.ThirdPartyCookieMode = CookieControlsMode.BlockThirdParty;
```

**VB**
```vb
Dim profile As IProfile = engine.Profiles.Default
profile.Preferences.ThirdPartyCookieMode = CookieControlsMode.BlockThirdParty
```



## Encryption

DotNetBrowser supports the cookie encryption by default. It uses the Chromium cookies encryption routines, so the cookies are stored the same way as in Chromium.

On Windows, DotNetBrowser uses only DPAPI to encrypt cookies. There are no alternatives at the moment.
