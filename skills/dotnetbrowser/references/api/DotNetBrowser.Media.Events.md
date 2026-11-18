# <a id="DotNetBrowser_Media_Events"></a> Namespace DotNetBrowser.Media.Events

### Classes

 [AudioCaptureEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs)

The base class for <xref href="DotNetBrowser.Media.IAudioCaptureSession" data-throw-if-not-resolved="false"></xref> related events.

 [AudioCaptureFailedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudioCaptureSession.Failed" data-throw-if-not-resolved="false"></xref> event.

 [AudioDataCapturedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioDataCapturedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudioCaptureSession.DataCaptured" data-throw-if-not-resolved="false"></xref> event.

 [AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs)

The base class for <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> related events.

 [AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStarted" data-throw-if-not-resolved="false"></xref> event.

 [AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStopped" data-throw-if-not-resolved="false"></xref> event.

## <a id="DotNetBrowser_Media_Events_AudioCaptureEventArgs"></a> Class AudioCaptureEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Media.IAudioCaptureSession" data-throw-if-not-resolved="false"></xref> related events.

```csharp
public abstract class AudioCaptureEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[AudioCaptureEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs)

##### Derived

[AudioCaptureFailedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs), 
[AudioDataCapturedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioDataCapturedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_Events_AudioCaptureEventArgs_Session"></a> Session

Gets the <xref href="DotNetBrowser.Media.IAudioCaptureSession" data-throw-if-not-resolved="false"></xref> instance that initiated this event.

```csharp
public IAudioCaptureSession Session { get; }
```

##### Property Value

 [IAudioCaptureSession](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudioCaptureSession)

## <a id="DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs"></a> Class AudioCaptureFailedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudioCaptureSession.Failed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioCaptureFailedEventArgs : AudioCaptureEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[AudioCaptureEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs) ← 
[AudioCaptureFailedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs)

##### Inherited Members

[AudioCaptureEventArgs.Session](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs_Session), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_Events_AudioCaptureFailedEventArgs_ErrorMessage"></a> ErrorMessage

Gets the message describing the cause of the failure.

```csharp
public string ErrorMessage { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Media_Events_AudioDataCapturedEventArgs"></a> Class AudioDataCapturedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudioCaptureSession.DataCaptured" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioDataCapturedEventArgs : AudioCaptureEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[AudioCaptureEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs) ← 
[AudioDataCapturedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioDataCapturedEventArgs)

##### Inherited Members

[AudioCaptureEventArgs.Session](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioCaptureEventArgs_Session), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

The buffer contains <xref href="DotNetBrowser.Media.Events.AudioDataCapturedEventArgs.FrameCount" data-throw-if-not-resolved="false"></xref> frames in the format set by the
<xref href="DotNetBrowser.Media.AudioCaptureOptions" data-throw-if-not-resolved="false"></xref> of the session. Samples are 32-bit floating-point values, stored
separately for each channel.

### Properties

#### <a id="DotNetBrowser_Media_Events_AudioDataCapturedEventArgs_ChannelCount"></a> ChannelCount

Gets the number of channels in this buffer.

```csharp
public int ChannelCount { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

The order of the channels is defined by the <xref href="DotNetBrowser.Media.AudioCaptureOptions.ChannelLayout" data-throw-if-not-resolved="false"></xref> of the
session.

#### <a id="DotNetBrowser_Media_Events_AudioDataCapturedEventArgs_FrameCount"></a> FrameCount

Gets the number of frames in this buffer.

```csharp
public int FrameCount { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

Each frame contains one sample per channel.

#### <a id="DotNetBrowser_Media_Events_AudioDataCapturedEventArgs_Timestamp"></a> Timestamp

Gets the time from the first captured frame of the session to the first frame of this buffer.

```csharp
public TimeSpan Timestamp { get; }
```

##### Property Value

 [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

##### Remarks

Buffers follow each other without gaps, so the timestamps grow by the buffer duration. A larger step
means that the audio between the buffers was lost.

### Methods

#### <a id="DotNetBrowser_Media_Events_AudioDataCapturedEventArgs_GetChannelData_System_Int32_"></a> GetChannelData\(int\)

Returns the samples of the given channel.

```csharp
public float[] GetChannelData(int channel)
```

##### Parameters

`channel` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The index of the channel, from zero to <xref href="DotNetBrowser.Media.Events.AudioDataCapturedEventArgs.ChannelCount" data-throw-if-not-resolved="false"></xref> - 1.

##### Returns

 [float](https://learn.microsoft.com/dotnet/api/system.single)\[\]

A new array with <xref href="DotNetBrowser.Media.Events.AudioDataCapturedEventArgs.FrameCount" data-throw-if-not-resolved="false"></xref> samples of the channel.

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

<code class="paramref">channel</code> is out of range.

## <a id="DotNetBrowser_Media_Events_AudioEventArgs"></a> Class AudioEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> related events.

```csharp
public class AudioEventArgs : BrowserEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs)

##### Derived

[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs), 
[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

##### Inherited Members

[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_Events_AudioEventArgs_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance that initiated this event.

```csharp
public IAudio Audio { get; }
```

##### Property Value

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

## <a id="DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs"></a> Class AudioPlaybackStartedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioPlaybackStartedEventArgs : AudioEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs) ← 
[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs)

##### Inherited Members

[AudioEventArgs.Audio](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs_Audio), 
[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs"></a> Class AudioPlaybackStoppedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStopped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioPlaybackStoppedEventArgs : AudioEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs) ← 
[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

##### Inherited Members

[AudioEventArgs.Audio](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs_Audio), 
[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)
