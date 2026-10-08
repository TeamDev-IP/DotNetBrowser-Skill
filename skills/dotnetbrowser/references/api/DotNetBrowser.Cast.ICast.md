# <a id="DotNetBrowser_Cast_ICast"></a> Interface ICast

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that provides access for casting media on receivers.

```csharp
public interface ICast
```

## Properties

### <a id="DotNetBrowser_Cast_ICast_StartPresentationHandler"></a> StartPresentationHandler

Gets or sets a handler that is used when a presentation has been requested via the JavaScript
Presentation API.

```csharp
IHandler<StartPresentationParameters, StartPresentationResponse> StartPresentationHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[StartPresentationParameters](DotNetBrowser.Cast.Handlers.StartPresentationParameters.md), [StartPresentationResponse](DotNetBrowser.Cast.Handlers.StartPresentationResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse.Start(DotNetBrowser.Cast.IMediaReceiver)" data-throw-if-not-resolved="false"></xref> method to
    use the given <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.
</p>
<p>
    Use the<xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse.Cancel" data-throw-if-not-resolved="false"></xref> method
    if the cast session request should be canceled.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be
    applied - the method <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    Presentation API is available only in secure contexts (HTTPS).
</p>
<p>
    The callback can be invoked only if media routing is
    <xref href="DotNetBrowser.Engine.EngineOptions.IsMediaRoutingEnabled" data-throw-if-not-resolved="false"></xref> enabled.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Cast_ICast_CastContent_DotNetBrowser_Cast_IMediaReceiver_"></a> CastContent\(IMediaReceiver\)

Starts casting the browser content to <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref>.

```csharp
Task<ICastSession> CastContent(IMediaReceiver receiver)
```

#### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

media receiver for casting.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.ICastSession.md)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

#### Remarks

<p>
    In case when the web page has the default JavaScript PresentationRequest:

<pre><code class="lang-csharp">const presentationRequest = new PresentationRequest(['receiver/index.html']);
navigator.presentation.defaultRequest = presentationRequest;</code></pre>

</p>
<p>
    The presentation of the media content specified in this request is started instead of
    casting the browser content. This implies that the receiver should
    <xref href="DotNetBrowser.Cast.IMediaReceiver.Supports(DotNetBrowser.Cast.CastMode%2cDotNetBrowser.Cast.PresentationRequest)" data-throw-if-not-resolved="false"></xref> support the presentation
    as a media source. Otherwise, if there is no default JavaScript PresentationRequest, the receiver
    should <xref href="DotNetBrowser.Cast.IMediaReceiver.Supports(DotNetBrowser.Cast.CastMode%2cDotNetBrowser.Cast.PresentationRequest)" data-throw-if-not-resolved="false"></xref> support any browser's
    content as <xref href="DotNetBrowser.Cast.CastMode.Browser" data-throw-if-not-resolved="false"></xref> media source.
</p>

#### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.MediaRoutingException.md)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

### <a id="DotNetBrowser_Cast_ICast_CastScreen_DotNetBrowser_Cast_IMediaReceiver_"></a> CastScreen\(IMediaReceiver\)

Starts casting screen's content by selecting the screen in the picker dialog.

```csharp
Task<ICastSession> CastScreen(IMediaReceiver receiver)
```

#### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

media receiver for casting.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.ICastSession.md)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

#### Remarks

<p>
    The receiver should support the <xref href="DotNetBrowser.Cast.CastMode.Screen" data-throw-if-not-resolved="false"></xref> cast mode.
</p>

#### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.MediaRoutingException.md)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

### <a id="DotNetBrowser_Cast_ICast_CastScreen_DotNetBrowser_Cast_IMediaReceiver_DotNetBrowser_Cast_ScreenCastOptions_"></a> CastScreen\(IMediaReceiver, ScreenCastOptions\)

Starts casting the screen's content to the media receiver.

```csharp
Task<ICastSession> CastScreen(IMediaReceiver receiver, ScreenCastOptions options)
```

#### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

media receiver for casting.

`options` [ScreenCastOptions](DotNetBrowser.Cast.ScreenCastOptions.md)

screen cast options for casting.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.ICastSession.md)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

#### Remarks

<p>
    The receiver should support the <xref href="DotNetBrowser.Cast.CastMode.Screen" data-throw-if-not-resolved="false"></xref> cast mode.
</p>

#### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.MediaRoutingException.md)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

### <a id="DotNetBrowser_Cast_ICast_DefaultPresentationRequest"></a> DefaultPresentationRequest\(\)

The default JavaScript <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref> specified on the page.

<p>
    Usually, the default <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref> is specified on resources like YouTube.
    The developer can specify it this way:

<pre><code class="lang-csharp">const presentationRequest = new PresentationRequest(['receiver/index.html']);
navigator.presentation.defaultRequest = presentationRequest;</code></pre>

</p>

```csharp
PresentationRequest DefaultPresentationRequest()
```

#### Returns

 [PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md)

The instance of the default JavaScript <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref>.

