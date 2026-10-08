# <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters"></a> Class SelectMediaDeviceParameters

Namespace: [DotNetBrowser.Media.Handlers](DotNetBrowser.Media.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Media.IMediaDevices.SelectMediaDeviceHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class SelectMediaDeviceParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectMediaDeviceParameters](DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_Devices"></a> Devices

Gets the collection of the available media stream devices of the requested <xref href="DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.Type" data-throw-if-not-resolved="false"></xref>.

```csharp
public IEnumerable<MediaDevice> Devices { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MediaDevice](DotNetBrowser.Media.MediaDevice.md)\>

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_MediaDevices"></a> MediaDevices

Gets the <xref href="DotNetBrowser.Media.IMediaDevices" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public IMediaDevices MediaDevices { get; }
```

#### Property Value

 [IMediaDevices](DotNetBrowser.Media.IMediaDevices.md)

### <a id="DotNetBrowser_Media_Handlers_SelectMediaDeviceParameters_Type"></a> Type

Get the type of the requested media stream.

```csharp
public MediaDeviceType Type { get; }
```

#### Property Value

 [MediaDeviceType](DotNetBrowser.Media.MediaDeviceType.md)

