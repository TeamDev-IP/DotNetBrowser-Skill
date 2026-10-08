
# Migrating from 2.7 to 2.8

**Lead**
In this migration guide we describe what API has been removed/changed in 2.8 and what alternatives you should use instead.

## Updated API

### Cookie store

**v2.7**
Previously, it was necessary to pass the web page URL when setting a cookie:


**C#**
```csharp
Cookie cookie = new Cookie.Builder
{
    Name = "name",
    Value = "value",
    DomainName = ".google.com",
    Path = "/"
}.Build();
bool success = 
    engine.Profiles.Default.CookieStore.SetCookie("https://www.google.com",cookie).Result;
engine.Profiles.Default.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder With {
    .Name = "name",
    .Value = "value",
    .DomainName = ".google.com",
    .Path = "/"
}.Build()
Dim success As Boolean = 
    engine.Profiles.Default.CookieStore.SetCookie("https://www.google.com",cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



**v2.8**

`ICookieStore.SetCookie()` now has no URL parameter, as it was previously used for validation purposes only:


**C#**
```csharp
Cookie cookie = new Cookie.Builder(".google.com")
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
Dim cookie As Cookie = New Cookie.Builder(".google.com") With {
    .Name = "name",
    .Value = "value",
    .Path = "/"
}.Build()
Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



Specifying the domain name is now required.
In addition, `ICookieStore.Delete()` now returns a `Task` instead of `Task<bool>`.
