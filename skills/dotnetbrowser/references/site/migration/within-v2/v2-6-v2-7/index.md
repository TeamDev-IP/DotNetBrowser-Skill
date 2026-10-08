
# Migrating from 2.6 to 2.7

**Lead**
In this migration guide we describe what API has been removed/changed in 2.7 and what alternatives you should use instead.


## Removed API

### Loading HTML

**v2.6**

In certain cases, it was possible to load a simple HTML document using the `IFrame.LoadHtml()` or `IFrame.LoadData()`. Here is how it looked like: 


**C#**
```csharp
var html = "<html><head></head><body><h1>Hello world!</h1></body></html>";
browser.MainFrame.LoadHtml(html).Wait();
```

**VB**
```vb
Dim html = "<html><head></head><body><h1>Hello world!</h1></body></html>"
browser.MainFrame.LoadHtml(html).Wait()
```



**v2.7**

The security restrictions became more tight. As a result, when an HTML document relying on external scripts is loaded using `LoadHtml()`, it never loads those scripts and logs errors saying `Failed to load resource: net::ERR_NOT_IMPLEMENTED`. The same behavior could also be observed with images in HTML.

There is no way to fix this behavior without breaking the Chromium security, that's why both `IFrame.LoadHtml` and `IFrame.LoadData` were removed completely from the API. 

The possible workaround is to use `data:` encoded URI and then load it using the regular LoadUrl call. Here is an example:


**C#**
```csharp
var html = "<html><head></head><body><h1>Html Encoded in URL!</h1></body></html>";
var base64EncodedHtml = Convert.ToBase64String(Encoding.UTF8.GetBytes(html));
browser.Navigation.LoadUrl("data:text/html;base64," + base64EncodedHtml).Wait();
```

**VB**
```vb
Dim html = "<html><head></head><body><h1>Html Encoded in URL!</h1></body></html>"
Dim base64EncodedHtml = Convert.ToBase64String(Encoding.UTF8.GetBytes(html))
browser.Navigation.LoadUrl("data:text/html;base64," & base64EncodedHtml).Wait()
```



However, the base URL cannot be set when using this workaround.

Another possible approach is to register a `Scheme` with a handler and intercept the corresponding request to provide the HTML. See the corresponding [article](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme).

## Updated API

### Cookie store

**v2.6**
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

bool success = engine.CookieStore.SetCookie("https://www.google.com",cookie).Result;
engine.CookieStore.Flush();
```

**VB**
```vb
Dim cookie As Cookie = New Cookie.Builder With {
    .Name = "name",
    .Value = "value",
    .DomainName = ".google.com",
    .Path = "/"
}.Build()

Dim success As Boolean = engine.CookieStore.SetCookie("https://www.google.com",cookie).Result
engine.CookieStore.Flush()
```



**v2.7**

`ICookieStore.SetCookie()` now has no URL parameter, as it was previously used for validation purposes only:


**C#**
```csharp
Cookie cookie = new Cookie.Builder
{
    Name = "name",
    Value = "value",
    DomainName = ".google.com",
    Path = "/"
}.Build();

bool success = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result;
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

Dim success As Boolean = engine.Profiles.Default.CookieStore.SetCookie(cookie).Result
engine.Profiles.Default.CookieStore.Flush()
```



In addition, `ICookieStore.Delete()` now returns a `Task` instead of `Task<bool>`.

## Added API 

### Default background color

When Chromium does not know the background color of a web page, or the color has not been specified at all, it uses the white color. In 2.7 we extended the API with new functionality that allows you to configure the default background color that Chromium should use instead of the default white color in such cases.

The following code demonstrates how to set the desired background color for about:blank page:


**C#**
```csharp
Color purple = new Color(0.6f, 0.3f, 0.6f);
browser.Settings.DefaultBackgroundColor = purple;
```

**VB**
```vb
Dim purple As New Color(0.6F, 0.3F, 0.6F)
browser.Settings.DefaultBackgroundColor = purple
```



### Get frame contents as text

The `IFrame.Text` property returns the content of the frame and its sub-frames as plain text:


**C#**
```csharp
string text = browser.MainFrame?.Text;
```

**VB**
```vb
Dim text As String = browser.MainFrame?.Text
```



### View page source

Now you can view source of the loaded web page or frame like in Google Chrome via `IFrame.ViewSource`:


**C#**
```csharp
browser.MainFrame?.ViewSource();
```

**VB**
```vb
browser.MainFrame?.ViewSource()
```



The code above tells Chromium to create and open a new popup window with the HTML source of the main frame.

### JavaScript `Promise` support

Now you can can work with the JavaScript promises directly without a need to create a wrapper over `IJsObject`. For example:


**C#**
```csharp
IJsPromise promise = browser.MainFrame
                            .ExecuteJavaScript<IJsPromise>("Promise.resolve(\"test\")")
                            .Result;

// Invoke some .NET code when the promise is fulfilled or rejected.
promise.Then(o => Console.WriteLine("Promise fulfilled"),
             e => Console.WriteLine("Promise rejected"));
```

**VB**
```vb
Dim promise As IJsPromise = 
    browser.MainFrame
            .ExecuteJavaScript(Of IJsPromise)("Promise.resolve(""test"")")
            .Result

' Invoke some .NET code when the promise is fulfilled or rejected.
promise.Then(Sub(o) Console.WriteLine("Promise fulfilled"), 
             Sub(e) Console.WriteLine("Promise rejected"))
```



### Preferred color scheme

It is possible to force the preferred color scheme via browser settings:


**C#**
```csharp
// Forces dark mode.
browser.Settings.PreferredColorScheme = PreferredColorScheme.Dark;
// Forces light mode.
browser.Settings.PreferredColorScheme = PreferredColorScheme.Light;
```

**VB**
```vb
' Forces dark mode.
browser.Settings.PreferredColorScheme = PreferredColorScheme.Dark 
' Forces light mode.
browser.Settings.PreferredColorScheme = PreferredColorScheme.Light 
```



The websites which respect the `prefers-color-scheme` media query will switch to the light or dark mode accordingly.

### Chromium profiles support

Each Engine has a default `Profile` you can access via:


**C#**
```csharp
IProfile defaultProfile = engine.Profiles.Default;
```

**VB**
```vb
Dim defaultProfile As IProfile = engine.Profiles.Default
```



The below services now belong to `Profile`. You can manage cookies, downloads, permissions, plugins, etc. independently for every profile:

- `ZoomLevels`
- `Plugins`
- `Proxy`
- `Network`
- `SpellChecker`
- `CookieStore`
- `HttpCache`
- `Downloads`
- `Permissions`

Find out more in the corresponding [guide](https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/).
