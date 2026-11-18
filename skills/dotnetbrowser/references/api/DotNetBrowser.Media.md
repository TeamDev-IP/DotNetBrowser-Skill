# <a id="DotNetBrowser_Media"></a> Namespace DotNetBrowser.Media

### Namespaces

 [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)

 [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)

### Classes

 [AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)

The options of an audio capture session.

 [MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)

The details of the media input device (audio/video).

### Interfaces

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

Allows controlling audio on the loaded web page and receive notifications when audio has been
started or stopped playing.

 [IAudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureOptions)

The read-only options of an audio capture session.

 [IAudioCaptureSession](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession)

A session that captures the audio of a browser.

 [IMediaDevices](DotNetBrowser.Media.md#DotNetBrowser_Media_IMediaDevices)

An engine service that allows accessing all the available media input devices.

### Enums

 [AudioChannelLayout](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioChannelLayout)

The number and the order of the captured audio channels.

 [MediaDeviceType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDeviceType)

The media device types.

 [MediaType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaType)

List of the known media types. It's used in <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuParameters" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Media_AudioCaptureOptions"></a> Class AudioCaptureOptions

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The options of an audio capture session.

```csharp
public sealed class AudioCaptureOptions : IAudioCaptureOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)

##### Implements

[IAudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    A captured buffer must last from 10 to 500 milliseconds, that is, <xref href="DotNetBrowser.Media.AudioCaptureOptions.FramesPerBuffer" data-throw-if-not-resolved="false"></xref>
    must be from a hundredth to a half of <xref href="DotNetBrowser.Media.AudioCaptureOptions.SampleRate" data-throw-if-not-resolved="false"></xref>. This rule is checked when the
    options are passed to <xref href="DotNetBrowser.Media.IAudio.StartCapture(DotNetBrowser.Media.AudioCaptureOptions)" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    A started session keeps a read-only copy of these options in
    <xref href="DotNetBrowser.Media.IAudioCaptureSession.Options" data-throw-if-not-resolved="false"></xref>, so changing this instance afterwards affects only the
    sessions started with it later.
</p>

### Fields

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_DefaultFramesPerBuffer"></a> DefaultFramesPerBuffer

The default number of frames per captured buffer.

```csharp
public static readonly int DefaultFramesPerBuffer
```

##### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_DefaultSampleRate"></a> DefaultSampleRate

The default sample rate in hertz.

```csharp
public static readonly int DefaultSampleRate
```

##### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_MaxSampleRate"></a> MaxSampleRate

The maximum supported sample rate in hertz.

```csharp
public static readonly int MaxSampleRate
```

##### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_MinSampleRate"></a> MinSampleRate

The minimum supported sample rate in hertz.

```csharp
public static readonly int MinSampleRate
```

##### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Properties

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_ChannelLayout"></a> ChannelLayout

Gets or sets the channel layout of the captured audio.

```csharp
public AudioChannelLayout ChannelLayout { get; set; }
```

##### Property Value

 [AudioChannelLayout](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioChannelLayout)

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The value is not a defined <xref href="DotNetBrowser.Media.AudioChannelLayout" data-throw-if-not-resolved="false"></xref>.

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_FramesPerBuffer"></a> FramesPerBuffer

Gets or sets the number of frames in each captured buffer.

```csharp
public int FramesPerBuffer { get; set; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

Each frame contains one sample per channel.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The value is not positive.

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_MuteSource"></a> MuteSource

Gets or sets a value indicating whether the browser stops playing its audio while it is captured.

```csharp
public bool MuteSource { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

The captured audio is not affected. <xref href="DotNetBrowser.Media.IAudio.Muted" data-throw-if-not-resolved="false"></xref> keeps indicating whether the browser
was muted through that property.

#### <a id="DotNetBrowser_Media_AudioCaptureOptions_SampleRate"></a> SampleRate

Gets or sets the sample rate in hertz.

```csharp
public int SampleRate { get; set; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The value is less than <xref href="DotNetBrowser.Media.AudioCaptureOptions.MinSampleRate" data-throw-if-not-resolved="false"></xref> or greater than <xref href="DotNetBrowser.Media.AudioCaptureOptions.MaxSampleRate" data-throw-if-not-resolved="false"></xref>.

### See Also

[IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio).[StartCapture](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio_StartCapture_DotNetBrowser_Media_AudioCaptureOptions_)\([AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)\)

## <a id="DotNetBrowser_Media_MediaDevice"></a> Class MediaDevice

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The details of the media input device (audio/video).

```csharp
public sealed class MediaDevice
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_MediaDevice_Id"></a> Id

Gets the device's unique ID.

```csharp
public string Id { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Media_MediaDevice_Name"></a> Name

Gets the device's "friendly" name.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Media_MediaDevice_Type"></a> Type

Gets the device's type.

```csharp
public MediaDeviceType Type { get; }
```

##### Property Value

 [MediaDeviceType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDeviceType)

## <a id="DotNetBrowser_Media_IAudio"></a> Interface IAudio

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

Allows controlling audio on the loaded web page and receive notifications when audio has been
started or stopped playing.

```csharp
public interface IAudio : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Media_IAudio_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Media_IAudio_IsPlaying"></a> IsPlaying

Indicates if the audio is currently playing on the loaded web page.

```csharp
bool IsPlaying { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Media_IAudio_Muted"></a> Muted

Mutes or unmutes all audio output for this Browser instance.

```csharp
bool Muted { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Media_IAudio_StartCapture"></a> StartCapture\(\)

Starts capturing the audio of the browser with the default options.

```csharp
IAudioCaptureSession StartCapture()
```

##### Returns

 [IAudioCaptureSession](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession)

The started capture session.

##### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

Another capture session of this browser is active.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

##### See Also

[IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio).[StartCapture](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio_StartCapture_DotNetBrowser_Media_AudioCaptureOptions_)\([AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)\)

#### <a id="DotNetBrowser_Media_IAudio_StartCapture_DotNetBrowser_Media_AudioCaptureOptions_"></a> StartCapture\(AudioCaptureOptions\)

Starts capturing the audio of the browser.

```csharp
IAudioCaptureSession StartCapture(AudioCaptureOptions options)
```

##### Parameters

`options` [AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)

The options of the capture session. The session keeps a copy of them.

##### Returns

 [IAudioCaptureSession](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession)

The started capture session.

##### Remarks

<p>
    The session captures all audio the browser plays, including silence when nothing plays.
    Muting the browser with <xref href="DotNetBrowser.Media.IAudio.Muted" data-throw-if-not-resolved="false"></xref> does not affect the captured audio. The captured
    audio is silent when Chromium runs with the <code>--mute-audio</code> switch.
</p>
<p>
    While the session is active, Chromium treats the browser as visible, so the page is not
    throttled and its <code>document.visibilityState</code> is <code>visible</code>, and it keeps the display
    from going to sleep.
</p>
<p>
    The buffers captured before a <xref href="DotNetBrowser.Media.IAudioCaptureSession.DataCaptured" data-throw-if-not-resolved="false"></xref> handler is added
    are not delivered to it. To receive the audio from its beginning, add the handlers to the
    returned session before the page starts playing.
</p>
<p>
    A browser can have only one active capture session. Stop it before starting a new one.
</p>
<p>
    If the capture fails right after it starts, before the returned session can report the failure,
    the returned session is already disposed. Check <xref href="DotNetBrowser.IAutoDisposable.IsDisposed" data-throw-if-not-resolved="false"></xref> or
    <xref href="DotNetBrowser.Media.IAudioCaptureSession.IsActive" data-throw-if-not-resolved="false"></xref> if you need to know that the capture is running.
</p>

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">options</code> is <code>null</code>.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

A buffer described by <code class="paramref">options</code> is shorter than 10 or longer than 500
milliseconds, or the options are not supported.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

Another capture session of this browser is active.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Media_IAudio_AudioPlaybackStarted"></a> AudioPlaybackStarted

Occurs when an audio has been started playing on the web page.

```csharp
event EventHandler<AudioPlaybackStartedEventArgs> AudioPlaybackStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Media_IAudio_AudioPlaybackStopped"></a> AudioPlaybackStopped

Occurs when an audio has been stopped playing on the web page.

```csharp
event EventHandler<AudioPlaybackStoppedEventArgs> AudioPlaybackStopped
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Media_IAudioCaptureOptions"></a> Interface IAudioCaptureOptions

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The read-only options of an audio capture session.

```csharp
public interface IAudioCaptureOptions
```

### Remarks

The options of a session cannot be changed after the session is started. To capture in another format,
stop the session and start a new one with different <xref href="DotNetBrowser.Media.AudioCaptureOptions" data-throw-if-not-resolved="false"></xref>.

### Properties

#### <a id="DotNetBrowser_Media_IAudioCaptureOptions_ChannelLayout"></a> ChannelLayout

Gets the channel layout of the captured audio.

```csharp
AudioChannelLayout ChannelLayout { get; }
```

##### Property Value

 [AudioChannelLayout](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioChannelLayout)

#### <a id="DotNetBrowser_Media_IAudioCaptureOptions_FramesPerBuffer"></a> FramesPerBuffer

Gets the number of frames in each captured buffer.

```csharp
int FramesPerBuffer { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

Each frame contains one sample per channel.

#### <a id="DotNetBrowser_Media_IAudioCaptureOptions_MuteSource"></a> MuteSource

Indicates whether the browser stops playing its audio while it is captured.

```csharp
bool MuteSource { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Media_IAudioCaptureOptions_SampleRate"></a> SampleRate

Gets the sample rate in hertz.

```csharp
int SampleRate { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### See Also

[IAudioCaptureSession](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession).[Options](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession_Options)

## <a id="DotNetBrowser_Media_IAudioCaptureSession"></a> Interface IAudioCaptureSession

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

A session that captures the audio of a browser.

```csharp
public interface IAudioCaptureSession : IDisposable, IAutoDisposable
```

##### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

<p>
    The captured audio is delivered through the <xref href="DotNetBrowser.Media.IAudioCaptureSession.DataCaptured" data-throw-if-not-resolved="false"></xref> event. When the capture
    fails, the <xref href="DotNetBrowser.Media.IAudioCaptureSession.Failed" data-throw-if-not-resolved="false"></xref> event occurs and the session is disposed.
</p>
<p>
    The session is disposed when it is stopped, when it fails, and when the browser is disposed.
    Use the <xref href="DotNetBrowser.IAutoDisposable.Disposed" data-throw-if-not-resolved="false"></xref> event to learn that the session has ended for any
    of these reasons. Disposing the session stops the capture. Once the session is disposed, it drops
    the buffers it has not started delivering.
</p>

### Properties

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance whose audio is captured.

```csharp
IAudio Audio { get; }
```

##### Property Value

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_IsActive"></a> IsActive

Indicates whether this session is capturing audio.

```csharp
bool IsActive { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_Options"></a> Options

Gets the options this session was started with.

```csharp
IAudioCaptureOptions Options { get; }
```

##### Property Value

 [IAudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureOptions)

##### Remarks

The options cannot be changed while the session runs. To capture in another format, stop this
session and start a new one.

### Methods

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_Stop"></a> Stop\(\)

Stops the audio capture and disposes this session.

```csharp
void Stop()
```

##### Remarks

<p>
    When this method returns, a new session of the browser can be started.
</p>
<p>
    This method waits up to three seconds for a running <xref href="DotNetBrowser.Media.IAudioCaptureSession.DataCaptured" data-throw-if-not-resolved="false"></xref> or
    <xref href="DotNetBrowser.Media.IAudioCaptureSession.Failed" data-throw-if-not-resolved="false"></xref> handler to return.
</p>
<p>
    This method has no effect if the session is already disposed.
</p>

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_DataCaptured"></a> DataCaptured

Occurs when a buffer of audio has been captured.

```csharp
event EventHandler<AudioDataCapturedEventArgs> DataCaptured
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioDataCapturedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioDataCapturedEventArgs)\>

##### Remarks

<p>
    The buffers are delivered one by one, in the order they were captured, on a dedicated thread.
    Keep the handler fast: the buffers that wait for delivery are kept in memory.
</p>
<p>
    <xref href="DotNetBrowser.Media.IAudioCaptureSession.Stop" data-throw-if-not-resolved="false"></xref> and <xref href="System.IDisposable.Dispose" data-throw-if-not-resolved="false"></xref> wait up to three seconds for the running
    handler to return. A handler that runs longer may still be running after they return, so if it
    uses resources that you release after stopping the session, synchronize the handler with that code.
</p>
<p>
    Don't marshal from the handler synchronously to the thread that stops the session, for example
    with <code>Dispatcher.Invoke</code> or <code>Control.Invoke</code>: the wait then always takes the full three
    seconds. Use the asynchronous counterparts such as <code>Dispatcher.InvokeAsync</code> or
    <code>Control.BeginInvoke</code>.
</p>
<p>
    The buffers captured before the handler is added are not delivered to it.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudioCaptureSession" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Media_IAudioCaptureSession_Failed"></a> Failed

Occurs when the capture has failed.

```csharp
event EventHandler<AudioCaptureFailedEventArgs> Failed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioCaptureFailedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs)\>

##### Remarks

The session is disposed right after this event.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudioCaptureSession" data-throw-if-not-resolved="false"></xref> has already been disposed.

### See Also

[IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio).[StartCapture](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio_StartCapture_DotNetBrowser_Media_AudioCaptureOptions_)\([AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions)\)

## <a id="DotNetBrowser_Media_IMediaDevices"></a> Interface IMediaDevices

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

An engine service that allows accessing all the available media input devices.

```csharp
public interface IMediaDevices : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Media_IMediaDevices_AudioCaptureDevices"></a> AudioCaptureDevices

Gets a collection of the available audio capture devices.

```csharp
IEnumerable<MediaDevice> AudioCaptureDevices { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Media_IMediaDevices_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Media_IMediaDevices_SelectMediaDeviceHandler"></a> SelectMediaDeviceHandler

Gets or sets a handler that is used when the web page asks which media input device should be used.

```csharp
IHandler<SelectMediaDeviceParameters, SelectMediaDeviceResponse> SelectMediaDeviceHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SelectMediaDeviceParameters](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters), [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.Select(DotNetBrowser.Media.MediaDevice)" data-throw-if-not-resolved="false"></xref> to select a specific media input device.
</p>
<p>
    If there are no media input devices of the requested type (e.g. there are no video input
    devices), then the callback <b>will not be invoked</b>).
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>
<p>
    If the callback throws an exception or the returned media device is not the one from the
    <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.Devices" data-throw-if-not-resolved="false"></xref>, the system default media input device will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Media_IMediaDevices_VideoCaptureDevices"></a> VideoCaptureDevices

Gets a collection of the available video capture devices.

```csharp
IEnumerable<MediaDevice> VideoCaptureDevices { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Media_AudioChannelLayout"></a> Enum AudioChannelLayout

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The number and the order of the captured audio channels.

```csharp
public enum AudioChannelLayout
```

### Fields

`Mono = 1` 

One channel.



`Quad = 3` 

Four channels: front left, front right, back left, and back right.



`Stereo = 2` 

Two channels: left and right.



`Surround51 = 4` 

Six channels: front left, front right, center, low-frequency effects, side left, and side right.



`Surround71 = 5` 

Eight channels: front left, front right, center, low-frequency effects, back left, back right,
side left, and side right.



### See Also

[AudioCaptureOptions](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions).[ChannelLayout](DotNetBrowser.Media.md#DotNetBrowser_Media_AudioCaptureOptions_ChannelLayout)

## <a id="DotNetBrowser_Media_MediaDeviceType"></a> Enum MediaDeviceType

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The media device types.

```csharp
public enum MediaDeviceType
```

### Fields

`AudioDevice = 2` 

An audio device.



`Unknown = 1` 

The media device type is unknown.



`VideoDevice = 3` 

A video device.

## <a id="DotNetBrowser_Media_MediaType"></a> Enum MediaType

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

List of the known media types. It's used in <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuParameters" data-throw-if-not-resolved="false"></xref>.

```csharp
public enum MediaType
```

### Fields

`Audio = 4` 

An audio node is selected.



`Canvas = 5` 

A canvas node is selected.



`File = 6` 

A file node is selected.



`Image = 2` 

An image node is selected.



`None = 1` 

No special node is in context.



`Plugin = 7` 

A plugin node is selected.



`Video = 3` 

A video node is selected.
