# <a id="DotNetBrowser_Net_INetwork"></a> Interface INetwork

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Allows access and modifying to the network-level activities.

```csharp
public interface INetwork : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Net_INetwork_AcceptLanguage"></a> AcceptLanguage

Gets or sets the <code>Accept-Language</code> request header value.

```csharp
string AcceptLanguage { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Examples

<code>"fr, en-gb;q=0.8, en;q=0.7"</code> would mean: "I prefer French, but
will accept British English and other types of English."
Note, that all languages which are assigned a quality factor
greater than 0 are acceptable.

#### Remarks

This field restricts the set of natural languages that are preferred as a response to the request.
The default <code>Accept-Language</code> is <code>"en-us"</code>.
See <a href="https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html">https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html</a>
W3 Documentation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The value is set to null or an empty string.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_AuthenticateHandler"></a> AuthenticateHandler

Gets or sets a handler that is used when the website requests authentication.

```csharp
IHandler<AuthenticateParameters, AuthenticateResponse> AuthenticateHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[AuthenticateParameters](DotNetBrowser.Net.Handlers.AuthenticateParameters.md), [AuthenticateResponse](DotNetBrowser.Net.Handlers.AuthenticateResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Continue(System.String%2cSystem.String)" data-throw-if-not-resolved="false"></xref> method
    to continue authentication process.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method
    to cancel authentication process.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_CanAccessFileHandler"></a> CanAccessFileHandler

Gets or sets a handler that is used when the Chromium engine is about to access the requested file. Can be used
to disallow accessing the file.

```csharp
IHandler<CanAccessFileParameters, CanAccessFileResponse> CanAccessFileHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[CanAccessFileParameters](DotNetBrowser.Net.Handlers.CanAccessFileParameters.md), [CanAccessFileResponse](DotNetBrowser.Net.Handlers.CanAccessFileResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Can" data-throw-if-not-resolved="false"></xref> method
    to allow access to the file.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Cannot" data-throw-if-not-resolved="false"></xref> method
    to disallow access to the file.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Can" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_CanGetCookiesHandler"></a> CanGetCookiesHandler

Gets or sets a handler that is used when Chromium engine decides
whether cookies can be sent back to the web server.

```csharp
IHandler<CanGetCookiesParameters, CanGetCookiesResponse> CanGetCookiesHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.CanGetCookiesParameters.md), [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.CanGetCookiesResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Allow" data-throw-if-not-resolved="false"></xref> method to
    allow cookies to be sent to the web server.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Deny" data-throw-if-not-resolved="false"></xref> method to
    disallow cookies to be sent to the web server.
</p>
<p>
    If exception occurs inside the handler, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Allow" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_CanSetCookieHandler"></a> CanSetCookieHandler

Gets or sets a handler that is used when Chromium engine decides
whether cookie can be saved for the URL or not.

```csharp
IHandler<CanSetCookieParameters, CanSetCookieResponse> CanSetCookieHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[CanSetCookieParameters](DotNetBrowser.Net.Handlers.CanSetCookieParameters.md), [CanSetCookieResponse](DotNetBrowser.Net.Handlers.CanSetCookieResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Allow" data-throw-if-not-resolved="false"></xref> method to
    allow engine to save the cookie.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Deny" data-throw-if-not-resolved="false"></xref> method to
    deny engine to save the cookie. It will not be available
    via the <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> object.
</p>
<p>
    If exception occurs inside the handler, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Allow" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_HttpAuthPreferences"></a> HttpAuthPreferences

Gets the HTTP authorization preferences.

```csharp
IHttpAuthPreferences HttpAuthPreferences { get; }
```

#### Property Value

 [IHttpAuthPreferences](DotNetBrowser.Net.IHttpAuthPreferences.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Net_INetwork_ReceiveHeadersHandler"></a> ReceiveHeadersHandler

Gets or sets a handler that is used each time that an HTTP(S) response header is received. Due to redirects
and authentication requests this can happen multiple times per request. This event is intended
to allow adding, modifying, and deleting HTTP response headers, such as incoming "Set-Cookie" headers.

```csharp
IHandler<ReceiveHeadersParameters, ReceiveHeadersResponse> ReceiveHeadersHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.ReceiveHeadersParameters.md), [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.OverrideHeaders(System.Collections.Generic.IEnumerable%7bDotNetBrowser.Net.HttpHeader%7d)" data-throw-if-not-resolved="false"></xref> method to override headers.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.Continue" data-throw-if-not-resolved="false"></xref> method to continue without modifications.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_SendUploadDataHandler"></a> SendUploadDataHandler

Gets or sets a handler that is used when the upload data is about to send to the web server.
Can be used to override the upload data before it is sent.

```csharp
IHandler<SendUploadDataParameters, SendUploadDataResponse> SendUploadDataHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SendUploadDataParameters](DotNetBrowser.Net.Handlers.SendUploadDataParameters.md), [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)\>

#### Remarks

<p>
    Use one of the following methods to modify the upload data:

<ul>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.TextData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.FormData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.MultipartFormData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.BytesData)" data-throw-if-not-resolved="false"></xref>
        </li>
    </ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Continue" data-throw-if-not-resolved="false"></xref> method if you
    do not need to modify the upload data.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_SendUrlRequestHandler"></a> SendUrlRequestHandler

Gets or sets a handler that is used when an HTTP request is about to occur. It can be used to override the
requested URL and
redirect the request to another location.

```csharp
IHandler<SendUrlRequestParameters, SendUrlRequestResponse> SendUrlRequestHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SendUrlRequestParameters](DotNetBrowser.Net.Handlers.SendUrlRequestParameters.md), [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Override(System.String)" data-throw-if-not-resolved="false"></xref> method to
    override the requested URL.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Continue" data-throw-if-not-resolved="false"></xref> method to
    proceed without changes.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to
    cancel the request with the <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> error.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_StartTransactionHandler"></a> StartTransactionHandler

Gets or sets a handler that is used when the request is about to start the transaction process.
It allows adding, modifying, and deleting HTTP request headers.

```csharp
IHandler<StartTransactionParameters, StartTransactionResponse> StartTransactionHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[StartTransactionParameters](DotNetBrowser.Net.Handlers.StartTransactionParameters.md), [StartTransactionResponse](DotNetBrowser.Net.Handlers.StartTransactionResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.OverrideHeaders(System.Collections.Generic.IEnumerable%7bDotNetBrowser.Net.HttpHeader%7d)" data-throw-if-not-resolved="false"></xref> method
    to override headers.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.Continue" data-throw-if-not-resolved="false"></xref> method
    to continue with original headers.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_UserAgent"></a> UserAgent

Gets the default user-agent string.

```csharp
string UserAgent { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    The default user-agent string can be configured through the
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.UserAgent" data-throw-if-not-resolved="false"></xref> property. If the default
    user-agent string has not been specified, then this method returns a string obtained from the
    Chromium engine.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_VerifyCertificateHandler"></a> VerifyCertificateHandler

Gets or sets a handler that is used to verify the SSL certificate provided by the web server.

```csharp
IHandler<VerifyCertificateParameters, VerifyCertificateResponse> VerifyCertificateHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.VerifyCertificateParameters.md), [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Valid" data-throw-if-not-resolved="false"></xref> method if the SSL certificate
    should be accepted.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Invalid" data-throw-if-not-resolved="false"></xref> method if the SSL certificate
    must be rejected.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Default" data-throw-if-not-resolved="false"></xref> method to let Chromium decide
    whether
    SSL certificate should be accepted or rejected.
</p>
<p>
    If this method throws an exception, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Default" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

## Methods

### <a id="DotNetBrowser_Net_INetwork_CreateUrlRequestJob_DotNetBrowser_Net_UrlRequest_DotNetBrowser_Net_Handlers_UrlRequestJobOptions_"></a> CreateUrlRequestJob\(UrlRequest, UrlRequestJobOptions\)

Creates a new <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref> instance with the given <code class="paramref">options</code>.

<p>The URL request job is used to provide the response data for the intercepted URL request.</p>

```csharp
UrlRequestJob CreateUrlRequestJob(UrlRequest request, UrlRequestJobOptions options = null)
```

#### Parameters

`request` [UrlRequest](DotNetBrowser.Net.UrlRequest.md)

The intercepted <xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref> instance to bind the job with.

`options` [UrlRequestJobOptions](DotNetBrowser.Net.Handlers.UrlRequestJobOptions.md)

The options which are used to initialize the <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>

#### Returns

 [UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

A new <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_ConnectionTypeChanged"></a> ConnectionTypeChanged

Occurs when the network connection type has been changed.

```csharp
event EventHandler<ConnectionTypeChangedEventArgs> ConnectionTypeChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ConnectionTypeChangedEventArgs](DotNetBrowser.Net.Events.ConnectionTypeChangedEventArgs.md)\>

#### Remarks

<p>
    The event is raised whenever a change affects the route network packets
    take to any network server.
</p>
<p>
    For example, the event is triggered when:
</p>
<ul><li>A network connection becomes available or going away;</li><li>A VPN tunnel is established or taken down;</li><li>An active network connection's IP address changes.</li></ul>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_PacScriptErrorOccurred"></a> PacScriptErrorOccurred

Occurs when the error has been occured in the PAC script.

```csharp
event EventHandler<PacScriptErrorEventArgs> PacScriptErrorOccurred
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PacScriptErrorEventArgs](DotNetBrowser.Net.Events.PacScriptErrorEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_RedirectResponseCodeReceived"></a> RedirectResponseCodeReceived

Occurs when the redirect has been occured.

```csharp
event EventHandler<RedirectResponseCodeReceivedEventArgs> RedirectResponseCodeReceived
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.RedirectResponseCodeReceivedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_RequestCompleted"></a> RequestCompleted

Occurs when the request has been completed.

```csharp
event EventHandler<RequestCompletedEventArgs> RequestCompleted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RequestCompletedEventArgs](DotNetBrowser.Net.Events.RequestCompletedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_RequestDestroyed"></a> RequestDestroyed

Occurs when the request has been destroyed.

```csharp
event EventHandler<RequestDestroyedEventArgs> RequestDestroyed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RequestDestroyedEventArgs](DotNetBrowser.Net.Events.RequestDestroyedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_ResponseBytesReceived"></a> ResponseBytesReceived

Occurs when a part of HTTP response body has been received over the network.

```csharp
event EventHandler<ResponseBytesReceivedEventArgs> ResponseBytesReceived
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.ResponseBytesReceivedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_INetwork_ResponseStarted"></a> ResponseStarted

Occurs when the response has been started.

```csharp
event EventHandler<ResponseStartedEventArgs> ResponseStarted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ResponseStartedEventArgs](DotNetBrowser.Net.Events.ResponseStartedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

