# <a id="DotNetBrowser_Cookies_SameSite"></a> Enum SameSite

Namespace: [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)  
Assembly: DotNetBrowser.dll  

The SameSite cookie attribute values of the <code>Set-Cookie</code> HTTP response header. This attribute is used to
declare in which context the cookies can be sent.

```csharp
public enum SameSite
```

## Fields

`LaxMode = 2` 

The cookie can be sent with top-level navigations from a third-party site to the web site with the domain matching
the cookie. This is the default value in modern browsers.



`None = 3` 

The cookie can be sent in a third-party context. To use this mode the cookie must also be marked as secure.



`StrictMode = 1` 

The cookie can only be sent in a first-party context, when the cookie matches the domain of the current site.



