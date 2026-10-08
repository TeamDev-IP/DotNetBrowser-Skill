# <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse"></a> Class SelectMediaDeviceResponse

Namespace: [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SelectMediaDeviceResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the media device selection
is canceled.

```csharp
public static SelectMediaDeviceResponse Cancel()
```

#### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that it is allowed to list
the available media input devices.

```csharp
public static SelectMediaDeviceResponse Proceed()
```

#### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

#### Remarks

All media input devices of the requested type will be visible to JavaScript.

<p>
    For <code>getUserMedia()</code> calls, Chromium will select the most
    suitable available device and use it for the media stream.
</p>
<p>
    For <code>enumerateDevices()</code> calls, all available input devices will be
    included in the resulting device list.
</p>

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Select_DotNetBrowser_Media_MediaDevice_"></a> Select\(MediaDevice\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the given media input device
should be used.

```csharp
public static SelectMediaDeviceResponse Select(MediaDevice defaultDevice)
```

#### Parameters

`defaultDevice` [MediaDevice](DotNetBrowser.Media.MediaDevice.md)

The media device to use. Must be the one from the list of the media input devices
received from the <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.Devices" data-throw-if-not-resolved="false"></xref>. If an invalid device
is passed through this method, the first device from the list of media devices will be
used.

#### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

