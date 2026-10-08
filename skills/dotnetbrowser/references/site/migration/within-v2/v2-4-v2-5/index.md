
# Migrating from 2.4 to 2.5

**Lead**
In DotNetBrowser 2.5 the Chromium engine has been upgraded to version 88. This Chromium version has several breaking changes in the source code that affect the public API of product. In this migration guide we describe what API has been removed/changed in 2.5 and what alternatives you should use instead.


## Removed API

### Flash support

In Chromium 88 the Flash support is dropped, therefore, the following engine options became obsolete and were removed from the API:
 - `EngineOptions.PpapiFlashPath`
 - `EngineOptions.PpapiFlashVersion`

### UI languages

The following UI languages were removed, as they are no longer officially supported by Chromium:

- Afrikaans
- Chinese (HongKong)
- French (Canada)
- English (Australia)
- Zulu

## Added or updated API

### Network

#### Intercepting requests

**v2.4**

To intercept URL requests with the standard (e.g. `http`, `https`) and custom schemes (e.g. `my-app`) the `InterceptRequestHandler` was used. It allows intercepting requests and override response data as if it was sent from a web server.

Here is how to intercept requests with the `myscheme` scheme in 2.4:


**C#**
```csharp
engine.Network.InterceptRequestHandler =
    new Handler<InterceptRequestParameters, InterceptRequestResponse>(p =>
    {
        if(!p.UrlRequest.Url.StartsWith("myscheme"))
        {
            return InterceptRequestResponse.Proceed();
        }
        UrlRequestJobOptions options = new UrlRequestJobOptions
        {
            Headers = new List<HttpHeader>
            {
                new HttpHeader("Content-Type", "text/html", "charset=utf-8"),
            }
        };
        UrlRequestJob job = p.Network.CreateUrlRequestJob(p.UrlRequest, options);

        Task.Run(() =>
        {
            // The request processing is performed in a background thread
            // in order to avoid freezing the web page.
            job.Write(Encoding.UTF8.GetBytes("My data"));
            job.Complete();
        });
        
        return InterceptRequestResponse.Intercept(job);
    });

...

browser.Navigation.LoadUrl("myscheme://app/hello");
```

**VB**
```vb
engine.Network.InterceptRequestHandler = 
    New Handler(Of InterceptRequestParameters, InterceptRequestResponse)(Function(p)
        If Not p.UrlRequest.Url.StartsWith("myscheme") Then
            Return InterceptRequestResponse.Proceed()
        End If
        Dim options As New UrlRequestJobOptions With {
            .Headers = New List(Of HttpHeader) From {
                New HttpHeader("Content-Type", "text/html", "charset=utf-8")}
        }
        Dim job As UrlRequestJob = p.Network.CreateUrlRequestJob(p.UrlRequest, options)

        Task.Run(Sub()
            ' The request processing is performed in a background thread
            ' in order to avoid freezing the web page.
            job.Write(Encoding.UTF8.GetBytes("My data"))
            job.Complete()
        End Sub)

        Return InterceptRequestResponse.Intercept(job)
    End Function)

'...

browser.Navigation.LoadUrl("myscheme://app/hello")
```




**v2.5**

The previous approach with intercepting all requests has several security limitations and issues:

- the intercepted custom schemes are treated as non-standard, so you cannot intercept a custom scheme and return HTML with JavaScript that accesses `LocalStorage`. It will lead to the access denied error;
- not all schemes can be intercepted. For example, it is forbidden to intercept schemes such as `chrome`, `data`, or `chrome-extensions`. The previous version of the API allows doing this which might lead to unexpected behavior or crash inside Chromium;
- some schemes are treated as local schemes, e.g. `file`. They cannot be intercepted because it is not a network request.

In this version, we improved the API that allows intercepting URL requests and registering custom schemes. The new version does not have the security limitations and issues described above.

The following example demonstrates how to register the custom `myscheme` scheme and intercept all corresponding URL requests:


**C#**
```csharp
var handler = new Handler<InterceptRequestParameters, InterceptRequestResponse>(p =>
{
    UrlRequestJobOptions options = new UrlRequestJobOptions
    {
        Headers = new List<HttpHeader>
        {
            new HttpHeader("Content-Type", "text/html", "charset=utf-8"),
        }
    };
    UrlRequestJob job = p.Network.CreateUrlRequestJob(p.UrlRequest, options);

    Task.Run(() =>
    {
        // The request processing is performed in a background thread
        // in order to avoid freezing the web page.
        job.Write(Encoding.UTF8.GetBytes("My data"));
        job.Complete();
    });
    
    return InterceptRequestResponse.Intercept(job);
});

IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    Schemes =
    {
        { Scheme.Create("myscheme"), handler }
    }
}.Build());

IBrowser browser = engine.CreateBrowser();

browser.Navigation.LoadUrl("myscheme://app/hello");
```

**VB**
```vb
Dim handler As New Handler(
    Of InterceptRequestParameters, InterceptRequestResponse)(Function(p)
    Dim options As New UrlRequestJobOptions With {
        .Headers = New List(Of HttpHeader) From {
            New HttpHeader("Content-Type", "text/html", "charset=utf-8")}
    }
    Dim job As UrlRequestJob = p.Network.CreateUrlRequestJob(p.UrlRequest, options)

    Task.Run(Sub()
        ' The request processing is performed in a background thread
        ' in order to avoid freezing the web page.
        job.Write(Encoding.UTF8.GetBytes("My data"))
        job.Complete()
    End Sub)

    Return InterceptRequestResponse.Intercept(job)
End Function)

Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With {
    .Schemes = {
        { Scheme.Create("myscheme"), handler }
    }
}.Build())

Dim browser As IBrowser = engine.CreateBrowser()

browser.Navigation.LoadUrl("myscheme://app/hello")
```



**Note**
If the specified scheme cannot be intercepted, the corresponding exception will be thrown by the `EngineOptions` builder. For example: "The "file" scheme cannot be intercepted."


## Known limitations

The security restrictions became more tight in Chromium 88. As a result, when an HTML document relying on external scripts is loaded using `LoadHtml`, it never loads those scripts and logs errors saying `Failed to load resource: net::ERR_NOT_IMPLEMENTED`.

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
