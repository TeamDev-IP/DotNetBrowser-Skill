# <a id="DotNetBrowser_Media"></a> Namespace DotNetBrowser.Media

### Namespaces

 [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)

 [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)

### Classes

 [MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)

The details of the media input device (audio/video).

### Interfaces

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

Allows controlling audio on the loaded web page and receive notifications when audio has been
started or stopped playing.

 [IMediaDevices](DotNetBrowser.Media.md#DotNetBrowser_Media_IMediaDevices)

An engine service that allows accessing all the available media input devices.

### Enums

 [MediaDeviceType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDeviceType)

The media device types.

 [MediaType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaType)

List of the known media types. It's used in <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuParameters" data-throw-if-not-resolved="false"></xref>.

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
