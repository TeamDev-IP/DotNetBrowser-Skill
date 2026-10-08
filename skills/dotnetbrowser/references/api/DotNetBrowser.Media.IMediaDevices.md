# <a id="DotNetBrowser_Media_IMediaDevices"></a> Interface IMediaDevices

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

An engine service that allows accessing all the available media input devices.

```csharp
public interface IMediaDevices : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Media_IMediaDevices_AudioCaptureDevices"></a> AudioCaptureDevices

Gets a collection of the available audio capture devices.

```csharp
IEnumerable<MediaDevice> AudioCaptureDevices { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.MediaDevice.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Media_IMediaDevices_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Media_IMediaDevices_SelectMediaDeviceHandler"></a> SelectMediaDeviceHandler

Gets or sets a handler that is used when the web page asks which media input device should be used.

```csharp
IHandler<SelectMediaDeviceParameters, SelectMediaDeviceResponse> SelectMediaDeviceHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SelectMediaDeviceParameters](DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.md), [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Media_IMediaDevices_VideoCaptureDevices"></a> VideoCaptureDevices

Gets a collection of the available video capture devices.

```csharp
IEnumerable<MediaDevice> VideoCaptureDevices { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.MediaDevice.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> has already been disposed.

