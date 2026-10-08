# <a id="DotNetBrowser_Zoom_Events_LevelChangedEventArgs"></a> Class LevelChangedEventArgs

Namespace: [DotNetBrowser.Zoom.Events](DotNetBrowser.Zoom.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Zoom.IZoomLevels.LevelChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class LevelChangedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[LevelChangedEventArgs](DotNetBrowser.Zoom.Events.LevelChangedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Zoom_Events_LevelChangedEventArgs_Host"></a> Host

Gets the host of the URL of the web page which zoom level has been changed.

```csharp
public string Host { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Zoom_Events_LevelChangedEventArgs_Level"></a> Level

Gets the new zoom level of a web page.

```csharp
public Level Level { get; }
```

#### Property Value

 [Level](DotNetBrowser.Zoom.Level.md)

### <a id="DotNetBrowser_Zoom_Events_LevelChangedEventArgs_ZoomLevels"></a> ZoomLevels

Gets the <xref href="DotNetBrowser.Zoom.IZoomLevels" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
public IZoomLevels ZoomLevels { get; }
```

#### Property Value

 [IZoomLevels](DotNetBrowser.Zoom.IZoomLevels.md)

