# <a id="DotNetBrowser_Cookies"></a> Namespace DotNetBrowser.Cookies

### Classes

 [Cookie.Builder](DotNetBrowser.Cookies.Cookie.Builder.md)

A builder class to construct cookie.

 [Cookie](DotNetBrowser.Cookies.Cookie.md)

Represents an HTTP cookie.

### Interfaces

 [ICookieStore](DotNetBrowser.Cookies.ICookieStore.md)

The system for storing and retrieving cookies. The cookies can be stored in
the process memory (session cookies) or in files (persistent cookies).
The <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> instance provides access to both session and persistent cookies.

### Enums

 [SameSite](DotNetBrowser.Cookies.SameSite.md)

The SameSite cookie attribute values of the <code>Set-Cookie</code> HTTP response header. This attribute is used to
declare in which context the cookies can be sent.

