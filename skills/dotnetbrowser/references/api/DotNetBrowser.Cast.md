# <a id="DotNetBrowser_Cast"></a> Namespace DotNetBrowser.Cast

### Namespaces

 [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)

 [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)

### Classes

 [CastSessionStartFailedException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastSessionStartFailedException)

Thrown when the cast session start has been failed.

 [MediaRoutingException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaRoutingException)

Thrown when the media routing is disabled.

 [PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest)

The JavaScript 

<pre><code class="lang-csharp">PresentationRequest</code></pre>

.

 [ReceiverDisconnectedException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverDisconnectedException)

Thrown when the receiver has been disconnected.

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverNotDiscoveredException)

Thrown when the receiver has not been discovered within the specified timeout.

 [Screen](DotNetBrowser.Cast.md#DotNetBrowser_Cast_Screen)

The screen whose content can be cast.

 [ScreenCastOptions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ScreenCastOptions)

Configuration options for screen casting.

### Interfaces

 [ICast](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICast)

A service that provides access for casting media on receivers.

 [ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)

A session of casting media content to a media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

<p>
    The session is <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> discovered when the user starts casting
    the browser/screen content or a presentation of media content via the DotNetBrowser API, or another
    application, i.e.Google Chrome. To indicate that the cast session has been started by another
    profile and, accordingly, a Chromium instance the <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> property is provided.
</p>

 [ICastSessions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSessions)

A service that allows observing <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> cast
<xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> sessions.

 [IMediaCasting](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaCasting)

A service that provides access to all the required media casting services.

 [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

A media receiver to which media content can be cast.

<p>
    Usually, a media receiver is a device that supports the ChromeCast technology,
    but in Chromium's logic it can be even a wired display (HDMI, DVI, or similar).
</p>

 [IMediaReceivers](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceivers)

The service that allows observing media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receivers in the environment.

 [IScreens](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IScreens)

The service that allows obtaining connected screens whose content can be cast.

### Enums

 [AudioMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_AudioMode)

The audio casting mode for the content cast session.

 [CastMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastMode)

The types of content that can be cast to a media receiver.

 [MediaReceiverState](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaReceiverState)

The state of the media receiver.

 [ResultCode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ResultCode)

Contains the codes indicating the result of creating a cast session.

## <a id="DotNetBrowser_Cast_CastSessionStartFailedException"></a> Class CastSessionStartFailedException

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Thrown when the cast session start has been failed.

```csharp
public sealed class CastSessionStartFailedException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[CastSessionStartFailedException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastSessionStartFailedException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Cast_CastSessionStartFailedException__ctor_System_String_DotNetBrowser_Cast_ResultCode_"></a> CastSessionStartFailedException\(string, ResultCode\)

```csharp
public CastSessionStartFailedException(string message, ResultCode resultCode)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

`resultCode` [ResultCode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ResultCode)

### Properties

#### <a id="DotNetBrowser_Cast_CastSessionStartFailedException_ResultCode"></a> ResultCode

Gets the error code obtained from Chromium.

```csharp
public ResultCode ResultCode { get; }
```

##### Property Value

 [ResultCode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ResultCode)

## <a id="DotNetBrowser_Cast_MediaRoutingException"></a> Class MediaRoutingException

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Thrown when the media routing is disabled.

```csharp
public sealed class MediaRoutingException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[MediaRoutingException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaRoutingException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    Media routing can be enabled by setting <code>true</code> in the
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.MediaRoutingEnabled" data-throw-if-not-resolved="false"></xref> property.
</p>
<p>
    Should be set before the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance is created.
</p>

### Constructors

#### <a id="DotNetBrowser_Cast_MediaRoutingException__ctor"></a> MediaRoutingException\(\)

```csharp
public MediaRoutingException()
```

## <a id="DotNetBrowser_Cast_PresentationRequest"></a> Class PresentationRequest

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The JavaScript 

<pre><code class="lang-csharp">PresentationRequest</code></pre>

.

```csharp
public sealed class PresentationRequest : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_PresentationRequest_Frame"></a> Frame

Gets the frame from which the presentation has been requested.

```csharp
public IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

#### <a id="DotNetBrowser_Cast_PresentationRequest_OriginUrl"></a> OriginUrl

Gets the origin URL of the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> where the presentation
has been requested.

```csharp
public string OriginUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cast_PresentationRequest_PresentationUrls"></a> PresentationUrls

Gets all of URLs whose content will be cast.

```csharp
public IReadOnlyList<string> PresentationUrls { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

## <a id="DotNetBrowser_Cast_ReceiverDisconnectedException"></a> Class ReceiverDisconnectedException

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Thrown when the receiver has been disconnected.

```csharp
public sealed class ReceiverDisconnectedException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[ReceiverDisconnectedException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverDisconnectedException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Cast_ReceiverDisconnectedException__ctor_System_String_"></a> ReceiverDisconnectedException\(string\)

```csharp
public ReceiverDisconnectedException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Cast_ReceiverNotDiscoveredException"></a> Class ReceiverNotDiscoveredException

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Thrown when the receiver has not been discovered within the specified timeout.

```csharp
public sealed class ReceiverNotDiscoveredException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[ReceiverNotDiscoveredException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverNotDiscoveredException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Cast_ReceiverNotDiscoveredException__ctor"></a> ReceiverNotDiscoveredException\(\)

```csharp
public ReceiverNotDiscoveredException()
```

## <a id="DotNetBrowser_Cast_Screen"></a> Class Screen

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The screen whose content can be cast.

```csharp
public sealed class Screen
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Screen](DotNetBrowser.Cast.md#DotNetBrowser_Cast_Screen)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Screen_Name"></a> Name

Gets the screen whose content can be cast.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Cast_Screen_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cast_Screen_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Cast_ScreenCastOptions"></a> Class ScreenCastOptions

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Configuration options for screen casting.

```csharp
public sealed class ScreenCastOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ScreenCastOptions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ScreenCastOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_ScreenCastOptions_AudioMode"></a> AudioMode

Gets or sets the mode of casting audio during the content cast session.

```csharp
public AudioMode AudioMode { get; set; }
```

##### Property Value

 [AudioMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_AudioMode)

#### <a id="DotNetBrowser_Cast_ScreenCastOptions_Screen"></a> Screen

Gets or sets the screen to cast.

```csharp
public Screen Screen { get; set; }
```

##### Property Value

 [Screen](DotNetBrowser.Cast.md#DotNetBrowser_Cast_Screen)

## <a id="DotNetBrowser_Cast_ICast"></a> Interface ICast

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that provides access for casting media on receivers.

```csharp
public interface ICast
```

### Properties

#### <a id="DotNetBrowser_Cast_ICast_StartPresentationHandler"></a> StartPresentationHandler

Gets or sets a handler that is used when a presentation has been requested via the JavaScript
Presentation API.

```csharp
IHandler<StartPresentationParameters, StartPresentationResponse> StartPresentationHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[StartPresentationParameters](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationParameters), [StartPresentationResponse](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Cast_ICast_CastContent_DotNetBrowser_Cast_IMediaReceiver_"></a> CastContent\(IMediaReceiver\)

Starts casting the browser content to <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref>.

```csharp
Task<ICastSession> CastContent(IMediaReceiver receiver)
```

##### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

media receiver for casting.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

##### Remarks

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

##### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaRoutingException)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

#### <a id="DotNetBrowser_Cast_ICast_CastScreen_DotNetBrowser_Cast_IMediaReceiver_"></a> CastScreen\(IMediaReceiver\)

Starts casting screen's content by selecting the screen in the picker dialog.

```csharp
Task<ICastSession> CastScreen(IMediaReceiver receiver)
```

##### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

media receiver for casting.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

##### Remarks

<p>
    The receiver should support the <xref href="DotNetBrowser.Cast.CastMode.Screen" data-throw-if-not-resolved="false"></xref> cast mode.
</p>

##### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaRoutingException)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

#### <a id="DotNetBrowser_Cast_ICast_CastScreen_DotNetBrowser_Cast_IMediaReceiver_DotNetBrowser_Cast_ScreenCastOptions_"></a> CastScreen\(IMediaReceiver, ScreenCastOptions\)

Starts casting the screen's content to the media receiver.

```csharp
Task<ICastSession> CastScreen(IMediaReceiver receiver, ScreenCastOptions options)
```

##### Parameters

`receiver` [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

media receiver for casting.

`options` [ScreenCastOptions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ScreenCastOptions)

screen cast options for casting.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)\>

The task that represents the result of the asynchronous start of the cast session.
If the cast session has not been started, the task is completed with
<xref href="DotNetBrowser.Cast.CastSessionStartFailedException" data-throw-if-not-resolved="false"></xref>.
If the browser is closed during the casting start,the task will be canceled.

##### Remarks

<p>
    The receiver should support the <xref href="DotNetBrowser.Cast.CastMode.Screen" data-throw-if-not-resolved="false"></xref> cast mode.
</p>

##### Exceptions

 [MediaRoutingException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaRoutingException)

The media routing switch was not set for <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

#### <a id="DotNetBrowser_Cast_ICast_DefaultPresentationRequest"></a> DefaultPresentationRequest\(\)

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

##### Returns

 [PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest)

The instance of the default JavaScript <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Cast_ICastSession"></a> Interface ICastSession

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A session of casting media content to a media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

<p>
    The session is <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> discovered when the user starts casting
    the browser/screen content or a presentation of media content via the DotNetBrowser API, or another
    application, i.e.Google Chrome. To indicate that the cast session has been started by another
    profile and, accordingly, a Chromium instance the <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> property is provided.
</p>

```csharp
public interface ICastSession
```

### Properties

#### <a id="DotNetBrowser_Cast_ICastSession_Description"></a> Description

Gets the description of the session. Examples: "Mirroring tab (www.example.com)",
"Casting media", "Casting YouTube".

```csharp
string Description { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

The description may be empty when the session just started and Chromium didn't define the
cast content yet.

#### <a id="DotNetBrowser_Cast_ICastSession_IsAlive"></a> IsAlive

Indicates whether this cast session is alive.

```csharp
bool IsAlive { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cast_ICastSession_IsLocal"></a> IsLocal

Indicates whether this cast session is initiated and managed by the current
<xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref>.

```csharp
bool IsLocal { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Cast_ICastSession_MediaReceiver"></a> MediaReceiver

Gets the media receiver of this session.

```csharp
IMediaReceiver MediaReceiver { get; }
```

##### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

##### Remarks

<p>
    The method may block the current thread if the receiver is not discovered yet. It may
    happen when the cast session is not <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> local and started on the
    receiver not yet discovered by the current instance of Chromium.
</p>

#### <a id="DotNetBrowser_Cast_ICastSession_Mode"></a> Mode

Gets the mode of the session.

```csharp
CastMode Mode { get; }
```

##### Property Value

 [CastMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastMode)

### Methods

#### <a id="DotNetBrowser_Cast_ICastSession_Stop"></a> Stop\(\)

Stops the cast session.

```csharp
void Stop()
```

##### Remarks

<p>
    This method has no effect when this cast session is already stopped.
</p>

#### <a id="DotNetBrowser_Cast_ICastSession_Stopped"></a> Stopped

Occurs when a <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been stopped.

<p>
    Also, the cast session is stopped when the user starts a new cast session to the
    <xref href="DotNetBrowser.Cast.ICastSession.MediaReceiver" data-throw-if-not-resolved="false"></xref> receiver of this cast session.
</p>

```csharp
event EventHandler<CastSessionStoppedEventArgs> Stopped
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionStoppedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs)\>

## <a id="DotNetBrowser_Cast_ICastSessions"></a> Interface ICastSessions

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that allows observing <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> cast
<xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> sessions.

```csharp
public interface ICastSessions
```

### Properties

#### <a id="DotNetBrowser_Cast_ICastSessions_AllAlive"></a> AllAlive

Gets the list of <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> alive cast sessions.

```csharp
IReadOnlyList<ICastSession> AllAlive { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)\>

#### <a id="DotNetBrowser_Cast_ICastSessions_Discovered"></a> Discovered

Occurs when a new <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been discovered in
the environment.

```csharp
event EventHandler<CastSessionDiscoveredEventArgs> Discovered
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs)\>

#### <a id="DotNetBrowser_Cast_ICastSessions_StartFailed"></a> StartFailed

Occurs when a start of a <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been failed.

```csharp
event EventHandler<CastSessionStartFailedEventArgs> StartFailed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs)\>

## <a id="DotNetBrowser_Cast_IMediaCasting"></a> Interface IMediaCasting

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that provides access to all the required media casting services.

```csharp
public interface IMediaCasting
```

### Properties

#### <a id="DotNetBrowser_Cast_IMediaCasting_CastSessions"></a> CastSessions

Gets the service that allows observing alive cast sessions.

```csharp
ICastSessions CastSessions { get; }
```

##### Property Value

 [ICastSessions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSessions)

#### <a id="DotNetBrowser_Cast_IMediaCasting_Receivers"></a> Receivers

Gets the service that allows observing media receivers.

```csharp
IMediaReceivers Receivers { get; }
```

##### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceivers)

#### <a id="DotNetBrowser_Cast_IMediaCasting_Screens"></a> Screens

Gets the service that allows obtaining connected screens for casting.

```csharp
IScreens Screens { get; }
```

##### Property Value

 [IScreens](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IScreens)

## <a id="DotNetBrowser_Cast_IMediaReceiver"></a> Interface IMediaReceiver

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A media receiver to which media content can be cast.

<p>
    Usually, a media receiver is a device that supports the ChromeCast technology,
    but in Chromium's logic it can be even a wired display (HDMI, DVI, or similar).
</p>

```csharp
public interface IMediaReceiver
```

### Properties

#### <a id="DotNetBrowser_Cast_IMediaReceiver_Name"></a> Name

Gets the name of the receiver.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cast_IMediaReceiver_State"></a> State

Gets the current state of the receiver.

```csharp
MediaReceiverState State { get; }
```

##### Property Value

 [MediaReceiverState](DotNetBrowser.Cast.md#DotNetBrowser_Cast_MediaReceiverState)

### Methods

#### <a id="DotNetBrowser_Cast_IMediaReceiver_Supports_DotNetBrowser_Cast_CastMode_DotNetBrowser_Cast_PresentationRequest_"></a> Supports\(CastMode, PresentationRequest\)

Checks if the receiver supports casting of <xref href="DotNetBrowser.Cast.CastMode" data-throw-if-not-resolved="false"></xref>.

```csharp
bool Supports(CastMode castMode, PresentationRequest presentationRequest = null)
```

##### Parameters

`castMode` [CastMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastMode)

The parameter of the types of content that can be cast to a media receiver.

`presentationRequest` [PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest)

The parameter of the JavaScript PresentationRequest.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the receiver supports casting of <xref href="DotNetBrowser.Cast.CastMode" data-throw-if-not-resolved="false"></xref>, <code>false</code> otherwise.

##### Remarks

<p>
    The <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref> parameter should be set only for the
    <xref href="DotNetBrowser.Cast.CastMode.Presentation" data-throw-if-not-resolved="false"></xref> mode.
</p>

#### <a id="DotNetBrowser_Cast_IMediaReceiver_Disconnected"></a> Disconnected

Occurs when the receiver disconnected and is not observable by Chromium anymore.

```csharp
event EventHandler<MediaReceiverDisconnectedEventArgs> Disconnected
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaReceiverDisconnectedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs)\>

## <a id="DotNetBrowser_Cast_IMediaReceivers"></a> Interface IMediaReceivers

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The service that allows observing media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receivers in the environment.

```csharp
public interface IMediaReceivers
```

### Properties

#### <a id="DotNetBrowser_Cast_IMediaReceivers_AllAvailable"></a> AllAvailable

Gets the list of connected (not <xref href="DotNetBrowser.Cast.MediaReceiverState.Unavailable" data-throw-if-not-resolved="false"></xref> unavailable)
media receivers.

<p>
    The initial list of media receivers can be empty or not full. This is because receivers
    are <xref href="DotNetBrowser.Cast.Events.MediaReceiverDiscoveredEventArgs" data-throw-if-not-resolved="false"></xref> discovered asynchronously in Chromium.
</p>

```csharp
IReadOnlyList<IMediaReceiver> AllAvailable { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

### Methods

#### <a id="DotNetBrowser_Cast_IMediaReceivers_Refresh"></a> Refresh\(\)

Asynchronously updates the list of available media receivers.

<p>
    This method forces Chromium to discover media receivers available in the local network.
    Use it before calling the <xref href="DotNetBrowser.Cast.IMediaReceivers.RetrieveAsync(System.Predicate%7bDotNetBrowser.Cast.IMediaReceiver%7d%2cSystem.TimeSpan)" data-throw-if-not-resolved="false"></xref>
    method to shorten the time to discover new receivers.
</p>

```csharp
void Refresh()
```

#### <a id="DotNetBrowser_Cast_IMediaReceivers_RetrieveAsync_System_Predicate_DotNetBrowser_Cast_IMediaReceiver__System_TimeSpan_"></a> RetrieveAsync\(Predicate<IMediaReceiver\>, TimeSpan\)

Waiting till the first receiver matching the <code>predicate</code> is discovered.

```csharp
Task<IMediaReceiver> RetrieveAsync(Predicate<IMediaReceiver> predicate, TimeSpan timeout)
```

##### Parameters

`predicate` [Predicate](https://learn.microsoft.com/dotnet/api/system.predicate\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

The predicated media receiver.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The predefined timeout.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

The task that can be used to wait for completion and obtain the result with
the first discovered receiver matching the <code>predicate</code>.

##### Remarks

<p>
    If a matching receiver has already been discovered, returns it immediately.
</p>
<p>
    Example of usage:
</p>

<pre><code class="lang-csharp">browser.Cast.StartPresentationHandler =
    new AsyncHandler&lt;StartPresentationParameters, StartPresentationResponse&gt;(async p =&gt;
    {
        IMediaReceiver mediaReceiver
            = await p.MediaReceivers
                     .RetrieveAsync(receiver =&gt; receiver.Name.Contains("Samsung TV"), timeout);
        return StartPresentationResponse.Start(mediaReceiver);
    });</code></pre>

##### Exceptions

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverNotDiscoveredException)

When the receiver has not been discovered within <code>timeout</code>.

#### <a id="DotNetBrowser_Cast_IMediaReceivers_RetrieveAsync_System_Predicate_DotNetBrowser_Cast_IMediaReceiver__"></a> RetrieveAsync\(Predicate<IMediaReceiver\>\)

Waiting till the first receiver matching the <code>predicate</code> is discovered.

```csharp
Task<IMediaReceiver> RetrieveAsync(Predicate<IMediaReceiver> predicate)
```

##### Parameters

`predicate` [Predicate](https://learn.microsoft.com/dotnet/api/system.predicate\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

The predicated media receiver.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

The task that can be used to wait for completion and obtain the result with
the first discovered receiver matching the <code>predicate</code>.

##### Remarks

<p>
    If a matching receiver has already been discovered, returns it immediately.
</p>
<p>
    Example of usage:
</p>

<pre><code class="lang-csharp">browser.Cast.StartPresentationHandler =
    new AsyncHandler&lt;StartPresentationParameters, StartPresentationResponse&gt;(async p =&gt;
    {
        IMediaReceiver mediaReceiver
            = await p.MediaReceivers
                     .RetrieveAsync(receiver =&gt; receiver.Name.Contains("Samsung TV"));
        return StartPresentationResponse.Start(mediaReceiver);
    });</code></pre>

##### Exceptions

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ReceiverNotDiscoveredException)

When the receiver has not been discovered within 45 seconds.

#### <a id="DotNetBrowser_Cast_IMediaReceivers_Discovered"></a> Discovered

Occurs when a new media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver has been discovered in
the environment.

```csharp
event EventHandler<MediaReceiverDiscoveredEventArgs> Discovered
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaReceiverDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs)\>

## <a id="DotNetBrowser_Cast_IScreens"></a> Interface IScreens

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The service that allows obtaining connected screens whose content can be cast.

```csharp
public interface IScreens
```

### Properties

#### <a id="DotNetBrowser_Cast_IScreens_All"></a> All

Gets the list of connected screens whose content can be cast to a media receiver.

```csharp
IReadOnlyList<Screen> All { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Screen](DotNetBrowser.Cast.md#DotNetBrowser_Cast_Screen)\>

#### <a id="DotNetBrowser_Cast_IScreens_DefaultScreen"></a> DefaultScreen

Gets the default (main) screen.

```csharp
Screen DefaultScreen { get; }
```

##### Property Value

 [Screen](DotNetBrowser.Cast.md#DotNetBrowser_Cast_Screen)

## <a id="DotNetBrowser_Cast_AudioMode"></a> Enum AudioMode

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The audio casting mode for the content cast session.

```csharp
public enum AudioMode
```

### Fields

`Cast = 1` 

The audio content should be cast along with the video content.



`Ignore = 0` 

The audio content should not be cast along with the video content.

## <a id="DotNetBrowser_Cast_CastMode"></a> Enum CastMode

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The types of content that can be cast to a media receiver.

```csharp
public enum CastMode
```

### Fields

`Browser = 2` 

Cast the browser's web content.



`Presentation = 1` 

Cast the content specified by the presentation URLs or frame's origin provided via the
Presentation API.



`RemotePlayback = 4` 

Cast media content using the Remote Playback API.



`Screen = 3` 

Cast the screen's content.

## <a id="DotNetBrowser_Cast_MediaReceiverState"></a> Enum MediaReceiverState

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The state of the media receiver.

```csharp
public enum MediaReceiverState
```

### Fields

`Available = 1` 

The receiver is available to be cast to.



`Connected = 3` 

Content is currently cast to the receiver.



`Connecting = 2` 

The receiver is starting a new cast session. A receiver temporarily enters this
state when transitioning from Available to Connected.



`Disconnecting = 4` 

The receiver is still connected but is in the process of disconnecting. A receiver
temporarily enters this state when transitioning from Connected to Available.



`Unavailable = 5` 

The receiver is disconnected/cached (not available right now).

## <a id="DotNetBrowser_Cast_ResultCode"></a> Enum ResultCode

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Contains the codes indicating the result of creating a cast session.

```csharp
public enum ResultCode
```

### Fields

`Cancelled = 8` 

The cast session has been canceled, i.e. via the "Cancel" button in the screen picker.



`CastSessionAlreadyExists = 9` 

The cast session can not be created since it already exists.



`CastSessionAlreadyTerminated = 11` 

The cast session has already been terminated.



`CastSessionNotFound = 4` 

The cast session was not found.



`DesktopPickerFailed = 10` 

An attempt to show the screen picker has failed.



`InvalidOrigin = 6` 

The origin of the web content is not allowed to start a cast session.



`NoSupportedProvider = 7` 

The media source provider is not supported.



`NotificationDisabled = 14` 

Failed to launch session as the notifications are disabled on the receiver device.



`Ok = 2` 

The cast session successfully started.



`ReceiverNotFound = 5` 

The receiver was not found when starting the cast session.



`RedundantRequest = 12` 

The cast request is redundant since the desired cast session is already active.



`TimedOut = 3` 

The cast session has not been created within the specified time.



`UnknownError = 1` 

The error is unknown.



`UserNotAllowed = 13` 

The user has declined the cast request.
