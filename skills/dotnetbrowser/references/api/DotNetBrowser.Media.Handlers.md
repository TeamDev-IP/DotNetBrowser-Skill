# <a id="DotNetBrowser_Media_Handlers"></a> Namespace DotNetBrowser.Media.Handlers

### Classes

 [SelectMediaDeviceParameters](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters)

The parameters of the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)

A response to the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters"></a> Class SelectMediaDeviceParameters

Namespace: [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class SelectMediaDeviceParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectMediaDeviceParameters](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_Devices"></a> Devices

Gets the collection of the available media stream devices of the requested <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.Type" data-throw-if-not-resolved="false"></xref>.

```csharp
public IEnumerable<MediaDevice> Devices { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)\>

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_MediaDevices"></a> MediaDevices

Gets the <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public IMediaDevices MediaDevices { get; }
```

##### Property Value

 [IMediaDevices](DotNetBrowser.Media.md#DotNetBrowser_Media_IMediaDevices)

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_Type"></a> Type

Get the type of the requested media stream.

```csharp
public MediaDeviceType Type { get; }
```

##### Property Value

 [MediaDeviceType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDeviceType)

## <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse"></a> Class SelectMediaDeviceResponse

Namespace: [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SelectMediaDeviceResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the media device selection
is canceled.

```csharp
public static SelectMediaDeviceResponse Cancel()
```

##### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that it is allowed to list
the available media input devices.

```csharp
public static SelectMediaDeviceResponse Proceed()
```

##### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

##### Remarks

All media input devices of the requested type will be visible to JavaScript.

<p>
    For <code>getUserMedia()</code> calls, Chromium will select the most
    suitable available device and use it for the media stream.
</p>
<p>
    For <code>enumerateDevices()</code> calls, all available input devices will be
    included in the resulting device list.
</p>

#### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse_Select_DotNetBrowser_Media_MediaDevice_"></a> Select\(MediaDevice\)

Creates a <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the given media input device
should be used.

```csharp
public static SelectMediaDeviceResponse Select(MediaDevice defaultDevice)
```

##### Parameters

`defaultDevice` [MediaDevice](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaDevice)

The media device to use. Must be the one from the list of the media input devices
received from the <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.Devices" data-throw-if-not-resolved="false"></xref>. If an invalid device
is passed through this method, the first device from the list of media devices will be
used.

##### Returns

 [SelectMediaDeviceResponse](DotNetBrowser.Media.Handlers.md#DotNetBrowser_Media_Handlers_SelectMediaDeviceResponse)

The <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.
