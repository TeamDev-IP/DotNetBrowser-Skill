# <a id="DotNetBrowser_Cast"></a> Namespace DotNetBrowser.Cast

### Namespaces

 [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)

 [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)

### Classes

 [CastSessionStartFailedException](DotNetBrowser.Cast.CastSessionStartFailedException.md)

Thrown when the cast session start has been failed.

 [MediaRoutingException](DotNetBrowser.Cast.MediaRoutingException.md)

Thrown when the media routing is disabled.

 [PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md)

The JavaScript 

<pre><code class="lang-csharp">PresentationRequest</code></pre>

.

 [ReceiverDisconnectedException](DotNetBrowser.Cast.ReceiverDisconnectedException.md)

Thrown when the receiver has been disconnected.

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.ReceiverNotDiscoveredException.md)

Thrown when the receiver has not been discovered within the specified timeout.

 [Screen](DotNetBrowser.Cast.Screen.md)

The screen whose content can be cast.

 [ScreenCastOptions](DotNetBrowser.Cast.ScreenCastOptions.md)

Configuration options for screen casting.

### Interfaces

 [ICast](DotNetBrowser.Cast.ICast.md)

A service that provides access for casting media on receivers.

 [ICastSession](DotNetBrowser.Cast.ICastSession.md)

A session of casting media content to a media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

<p>
    The session is <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> discovered when the user starts casting
    the browser/screen content or a presentation of media content via the DotNetBrowser API, or another
    application, i.e.Google Chrome. To indicate that the cast session has been started by another
    profile and, accordingly, a Chromium instance the <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> property is provided.
</p>

 [ICastSessions](DotNetBrowser.Cast.ICastSessions.md)

A service that allows observing <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> cast
<xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> sessions.

 [IMediaCasting](DotNetBrowser.Cast.IMediaCasting.md)

A service that provides access to all the required media casting services.

 [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

A media receiver to which media content can be cast.

<p>
    Usually, a media receiver is a device that supports the ChromeCast technology,
    but in Chromium's logic it can be even a wired display (HDMI, DVI, or similar).
</p>

 [IMediaReceivers](DotNetBrowser.Cast.IMediaReceivers.md)

The service that allows observing media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receivers in the environment.

 [IScreens](DotNetBrowser.Cast.IScreens.md)

The service that allows obtaining connected screens whose content can be cast.

### Enums

 [AudioMode](DotNetBrowser.Cast.AudioMode.md)

The audio casting mode for the content cast session.

 [CastMode](DotNetBrowser.Cast.CastMode.md)

The types of content that can be cast to a media receiver.

 [MediaReceiverState](DotNetBrowser.Cast.MediaReceiverState.md)

The state of the media receiver.

 [ResultCode](DotNetBrowser.Cast.ResultCode.md)

Contains the codes indicating the result of creating a cast session.

