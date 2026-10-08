# <a id="DotNetBrowser_Media_MediaDevice"></a> Class MediaDevice

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

The details of the media input device (audio/video).

```csharp
public sealed class MediaDevice
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MediaDevice](DotNetBrowser.Media.MediaDevice.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Media_MediaDevice_Id"></a> Id

Gets the device's unique ID.

```csharp
public string Id { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Media_MediaDevice_Name"></a> Name

Gets the device's "friendly" name.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Media_MediaDevice_Type"></a> Type

Gets the device's type.

```csharp
public MediaDeviceType Type { get; }
```

#### Property Value

 [MediaDeviceType](DotNetBrowser.Media.MediaDeviceType.md)

