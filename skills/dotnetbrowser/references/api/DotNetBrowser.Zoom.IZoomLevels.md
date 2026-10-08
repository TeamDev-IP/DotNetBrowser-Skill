# <a id="DotNetBrowser_Zoom_IZoomLevels"></a> Interface IZoomLevels

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the default zoom levels and receive notifications about zoom changes.

```csharp
public interface IZoomLevels : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Zoom_IZoomLevels_DefaultLevel"></a> DefaultLevel

Gets or sets the default zoom level for pages that don't override it.

```csharp
Level DefaultLevel { get; set; }
```

#### Property Value

 [Level](DotNetBrowser.Zoom.Level.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoomLevels" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Zoom_IZoomLevels_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Zoom_IZoomLevels_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Zoom_IZoomLevels_LevelChanged"></a> LevelChanged

Occurs when the zoom level for a specific URL has been changed.

```csharp
event EventHandler<LevelChangedEventArgs> LevelChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[LevelChangedEventArgs](DotNetBrowser.Zoom.Events.LevelChangedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoomLevels" data-throw-if-not-resolved="false"></xref> has already been disposed.

