
# Network

**Lead**
This guide shows how to work with the network-related functionality such as proxy, network events, authentication, TLS, client certificate authentication, etc.


The network-related functionality can be accessed through the `INetwork` instance that can be obtained using the `Profile.Network` property. Using `IEngine.Profiles.Default.Network` property you will get the `Network` instance associated with the default [`Profile`](https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/).

## Accept language

DotNetBrowser allows configuring the `Accept-Language` using the `INetwork.AcceptLanguage` property. The input parameter value represents the `Accept-Language` HTTP header value.

For example, the "fr, en-gb;q=0.8, en;q=0.7" value would mean: "I prefer French, but will accept British English, and other types of English":


**C#**
```csharp
network.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7";
```

**VB**
```vb
network.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7"
```



## ServerWhiteList

Since DotNetBrowser 1.9, you can configure HTTP server authorization whitelist that represents a string with comma/semicolon separated list of URLs. This feature allows you to use Integrated Windows authentication (IWA) and Kerberos authentication for the listed domains. 

With IWA, Chromium can authenticate the user to a web server or proxy without even prompting the user for a username or password. It does this by using cached credentials which are established when the user initially logs in to the machine that the browser is running on. IWA is supported for Negotiate and NTLM challenges only.

`ServerWhiteList` specifies which servers should be whitelisted for integrated authentication. By default, integrated authentication is only enabled when there is an authentication challenge from a proxy or from a server which is in this permitted list. If this list is not set, Chromium engine tries to detect if a server is on the _Intranet_ and responds to IWA requests only for _Intranet_ servers. If a server is detected as _Internet_, then IWA requests from this server are ignored.

`DelegateWhiteList` specifies the servers that Chromium may delegate to. If this list is not set, Chromium does not delegate user credentials even if a server is detected as _Intranet_.

If you specify multiple server names in the list, separate them with commas. Wildcards (*) are allowed.

**Note**
Since Chromium 81 integrated authentication is disabled for Incognito mode. In this case, the `AuthenticateHandler` handler will be invoked to supply username and password. Since DotNetBrowser 2.23.3 it is possible to override this behavior. For this purpose, it is necessary to add the `--ambient-authentication-in-private-modes-enabled` Chromium switch to override the [AmbientAuthenticationInPrivateModesEnabled](https://chromeenterprise.google/policies/#AmbientAuthenticationInPrivateModesEnabled) policy.


### HTTP server authorization whitelist

See the code sample below:


**C#**
```csharp
network.HttpAuthPreferences.ServerWhiteList = "*google.com,*example.com,*baz";
```

**VB**
```vb
network.HttpAuthPreferences.ServerWhiteList = "*google.com,*example.com,*baz"
```



### HTTP network delegate whitelist

See the code sample below:


**C#**
```csharp
network.HttpAuthPreferences.DelegateWhiteList = "*google.com,*example.com,*baz";
```

**VB**
```vb
network.HttpAuthPreferences.DelegateWhiteList = "*google.com,*example.com,*baz"
```



## TLS
### Certificate verification

By default, Chromium verifies all SSL certificates obtained from a web server during the web page loading. DotNetBrowser allows modifying this default behavior and take control over the verification process.

To handle certificate verification, use the `VerifyCertificateHandler` handler. Before it is invoked, Chromium verifies SSL certificate and provides the results of the verification to the handler. The handler receives the SSL certificate itself together with the verification results. You can verify the given SSL certificate and notify the engine whether to accept it or not. See the code sample below:


**C#**
```csharp
engine.Profiles.Default.Network.VerifyCertificateHandler
    = new Handler<VerifyCertificateParameters, VerifyCertificateResponse>(p =>
    {
        // SSL Certificate to verify.
        Certificate certificate = p.Certificate;
        // The results of the verification errors performed by default verifier.
        IEnumerable<CertificateVerificationError> certificateVerificationErrors =
            p.VerifyErrors;
        // The results of default verification should be used.
        return VerifyCertificateResponse.Default();
    });
```

**VB**
```vb
engine.Profiles.Default.Network.VerifyCertificateHandler = 
    New Handler(Of VerifyCertificateParameters, VerifyCertificateResponse)(Function(p)
        ' SSL Certificate to verify.
        Dim certificate As Certificate = p.Certificate
        ' The results of the verification errors performed by default verifier.
        Dim certificateVerificationErrors As IEnumerable(Of CertificateVerificationError) = 
            p.VerifyErrors
        ' The results of default verification should be used.
        Return VerifyCertificateResponse.Default()
    End Function)
```



### Client certificate authentication

DotNetBrowser supports authentication using HTTPS client certificates. Refer to the [Authentication](https://teamdev.com/dotnetbrowser/docs/guides/gs/authentication/#https-client-certificate) guide for details.

## Network events & handlers

The `INetwork` API defines a set of events and handlers that follow the life cycle of a web request. You can use these events to observe and analyze traffic. These handlers will allow you to intercept, block, or modify requests.

The event life cycle of successful requests looks as follows:
![Network Events Flow](https://teamdev.com/dotnetbrowser/img/articles/guides/network/network-events-flow.svg)

### Before URL request

The `SendUrlRequestHandler` handler is invoked when an HTTP request is about to occur. You can use this handler to override the URL and redirect the request to another location. For example:


**C#**
```csharp
network.SendUrlRequestHandler =
    new Handler<SendUrlRequestParameters, SendUrlRequestResponse>(p =>
    {
        return SendUrlRequestResponse.Override("<new-url>");
    });
```

**VB**
```vb
network.SendUrlRequestHandler = 
    New Handler(Of SendUrlRequestParameters, SendUrlRequestResponse)(Function(p)
        Return SendUrlRequestResponse.Override("<new-url>")
    End Function)
```



### Before send upload data

The `SendUploadDataHandler` handler is invoked before the upload data is sent to a web server. Here you can override the upload data. For example:


**C#**
```csharp
network.SendUploadDataHandler =
    new Handler<SendUploadDataParameters, SendUploadDataResponse>(p =>
    {
        return SendUploadDataResponse.Override("<text-data>");
    });
```

**VB**
```vb
network.SendUploadDataHandler = 
    New Handler(Of SendUploadDataParameters, SendUploadDataResponse)(Function(p)
        Return SendUploadDataResponse.Override("<text-data>")
    End Function)
```



**Note**
This handler will not be called if the request does not have the upload data.


The following upload data types are supported:

- `byte[]` represents a sequence of bytes;
- `string` - the data of the `text/plain` content type;
- `FormData` - the data of the `application/x-www-form-urlencoded` content type;
- `MultipartFormData` - the data of the `multipart/form-data` content type.

### Before start transaction

The `StartTransactionHandler` handler is invoked before the network transaction starts. You can add, modify, and delete the HTTP request headers before they are sent to a web server. See the code sample below:


**C#**
```csharp
network.StartTransactionHandler
    = new Handler<StartTransactionParameters, StartTransactionResponse>(p =>
    {
        IEnumerable<IHttpHeader> headers = p.Headers;
        List<HttpHeader> newHttpHeaders = headers.Cast<HttpHeader>().ToList();
        newHttpHeaders.Add(new HttpHeader("<header-name>", "<header-value>"));
        return StartTransactionResponse.OverrideHeaders(newHttpHeaders);
    });
```

**VB**
```vb
network.StartTransactionHandler = 
    New Handler(Of StartTransactionParameters, StartTransactionResponse)(Function(p)
        Dim headers As IEnumerable(Of IHttpHeader) = p.Headers
        Dim newHttpHeaders As List(Of HttpHeader) = 
            headers.Cast(Of HttpHeader)().ToList()
        newHttpHeaders.Add(New HttpHeader("<header-name>", "<header-value>"))
        Return StartTransactionResponse.OverrideHeaders(newHttpHeaders)
    End Function)
```



**Note**
The following headers are currently not provided to the handler:
<br>
<br>
- Authorization<br>
- Cache-Control<br>
- Connection<br>
- Content-Length<br>
- Host<br>
- If-Modified-Since<br>
- If-None-Match<br>
- If-Range<br>
- Partial-Data<br>
- Pragma<br>
- Proxy-Authorization<br>
- Proxy-Connection<br>
- Transfer-Encoding<br>

Note that we do not guarantee that this list is complete or stable.



### Receive headers

The `ReceiveHeadersHandler` handler is invoked for HTTP requests when the headers have been received. Here you can add, modify, or remove the HTTP headers received over the network. See the code sample below:


**C#**
```csharp
network.ReceiveHeadersHandler =
    new Handler<ReceiveHeadersParameters, ReceiveHeadersResponse>(p =>
    {
        IEnumerable<IHttpHeader> headers = p.Headers;
        List<HttpHeader> newHttpHeaders = headers.Cast<HttpHeader>().ToList();
        newHttpHeaders.Add(new HttpHeader("<header-name>", "<header-value>"));
        return ReceiveHeadersResponse.OverrideHeaders(newHttpHeaders);
    });
```

**VB**
```vb
network.ReceiveHeadersHandler = 
    New Handler(Of ReceiveHeadersParameters, ReceiveHeadersResponse)(Function(p)
        Dim headers As IEnumerable(Of IHttpHeader) = p.Headers
        Dim newHttpHeaders As List(Of HttpHeader) = 
            headers.Cast(Of HttpHeader)().ToList()
        newHttpHeaders.Add(New HttpHeader("<header-name>", "<header-value>"))
        Return ReceiveHeadersResponse.OverrideHeaders(newHttpHeaders)
    End Function)
```



### Redirect response code received

The `RedirectResponseCodeReceived` event occurs when a redirect response code `3xx` has been received for the request. You can get the details about the redirect such as new URL and response code. See the code sample below:


**C#**
```csharp
network.RedirectResponseCodeReceived += (s, e) => 
{
    string newUrl = e.NewUrl;
    int responseCode = e.ResponseCode;
};
```

**VB**
```vb
AddHandler network.RedirectResponseCodeReceived, Sub(s, e)
    Dim newUrl As String = e.NewUrl
    Dim responseCode As Integer = e.ResponseCode
End Sub
```



### Response started

The `ResponseStarted` event occurs when the first byte of the URL response body has been received. For HTTP requests, it means that the status line and the response headers are available. In this event, you can access the corresponding request and the response code. See the code sample below:


**C#**
```csharp
network.ResponseStarted += (s, e) => 
{
    UrlRequest urlRequest = e.UrlRequest;
    int responseCode = e.ResponseCode;
};
```

**VB**
```vb
AddHandler network.ResponseStarted, Sub(s, e)
    Dim urlRequest As UrlRequest = e.UrlRequest
    Dim responseCode As Integer = e.ResponseCode
End Sub
```



### Request completed

The `RequestCompleted` event occurs when the URL request has been successfully completed or failed. You can check whether the request has been started at all, get the details of the request state, and access the response code. See the code sample below:


**C#**
```csharp
network.RequestCompleted += (s, e) => 
{
    UrlRequest urlRequest = e.UrlRequest;
    // The details of the URL request state.
    RequestStatus urlRequestStatus = e.Status;
    // The HTTP response code.
    int responseCode = e.ResponseCode;
};
```

**VB**
```vb
AddHandler network.RequestCompleted, Sub(s, e)
    Dim urlRequest As UrlRequest = e.UrlRequest
    ' The details of the URL request state.
    Dim urlRequestStatus As RequestStatus = e.Status
    ' The HTTP response code.
    Dim responseCode As Integer = e.ResponseCode
End Sub
```



### Request destroyed

The `RequestDestroyed` event occurs when the request has been destroyed and it cannot be used anymore. To access the details of the destroyed request, use the following code:


**C#**
```csharp
network.RequestDestroyed += (s, e) => 
{
    UrlRequest urlRequest = e.UrlRequest;
};
```

**VB**
```vb
AddHandler network.RequestDestroyed, Sub(s, e)
    Dim urlRequest As UrlRequest = e.UrlRequest
End Sub
```



### Response bytes received

The `ResponseBytesReceived` event occurs when a part of HTTP response body is received over 
the network. It allows accessing the bytes of the HTTP response body:


**C#**
```csharp
network.ResponseBytesReceived += (s, e) => 
{
    byte[] data = e.Data;
};
```

**VB**
```vb
AddHandler network.ResponseBytesReceived, Sub(s, e)
    Dim data() As Byte = e.Data
End Sub
```



### PAC script error

The `PacScriptErrorOccurred` event occurs when there is an error in the PAC script. It allows obtaining the error details:


**C#**
```csharp
network.PacScriptErrorOccurred += (s, e) =>
{
    string errorText = e.ErrorText;
    uint lineNumber = e.LineNumber;
};
```

**VB**
```vb
AddHandler network.PacScriptErrorOccurred, Sub(s, e)
    Dim errorText As String = e.ErrorText
    Dim lineNumber As UInteger = e.LineNumber
End Sub
```



## Connection state

Chromium internally tracks the Internet connection status. When the Internet connection is dropped and then restored, Chromium detects this and programmatically reloads the currently loaded web page. You can get notifications when the network connection state is changed using this API:


**C#**
```csharp
profile.Network.ConnectionTypeChanged += (s, e) =>
{
    ConnectionType connectionType = e.ConnectionType;
};
```

**VB**
```vb
AddHandler profile.Network.ConnectionTypeChanged, Sub(s, e)
    Dim connectionType As ConnectionType = e.ConnectionType
End Sub
```


