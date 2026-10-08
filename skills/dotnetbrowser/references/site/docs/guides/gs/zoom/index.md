
# Zoom

**Lead**
This guide describes how to work with DotNetBrowser Zoom API.


DotNetBrowser allows to zoom content of a web page or all ones, receive notifications 
of web page zoom level change, override the default zoom level, and other features.

To work with the global zoom that will be applied to all web pages, use the `ZoomLevels` 
property available from [`engine.Profiles.Default`](https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/). For example:


**C#**
```csharp
IZoomLevels zoomLevels = engine.Profiles.Default.ZoomLevels;
```

**VB**
```vb
Dim zoomLevels As IZoomLevels = engine.Profiles.Default.ZoomLevels
```



If you need the `IZoomLevels` service associated with the default profile, use `engine.Profiles.Default.ZoomLevels`.

To control zoom of a web page loaded in the `IBrowser` instance, use the `IBrowser.Zoom` property.

## Default Zoom Level

The default zoom level for all web pages is 100%. You can change it using the `IZoomLevels.DefaultLevel` property.

The code sample below sets the default zoom level for all web pages to 150%:


**C#**
```csharp
engine.Profiles.Default.ZoomLevels.DefaultLevel = Level.P150;
```

**VB**
```vb
engine.Profiles.Default.ZoomLevels.DefaultLevel = Level.P150
```



## Zoom mode

By default, zoom is scoped to the origin of the loaded web page.
If two browsers in the same profile both display pages from
`https://example.com`, zooming in one of them changes the zoom
level in the other as well. This is the `ZoomMode.PerOrigin` mode.

If you want zoom to apply only to a specific browser, switch to
the `ZoomMode.PerBrowser` mode:


**C#**
```csharp
Browser.Zoom.Mode = ZoomMode.PerBrowser;
```

**VB**
```vb
Browser.Zoom.Mode = ZoomMode.PerBrowser
```



In this mode, changing the zoom level in one browser does not
affect other browsers, even when they display pages from the same
origin.

Changing the mode preserves the current zoom level. The mode can
be changed even when zoom is disabled — it takes effect when zoom
is enabled again.

To switch back to the default behavior:


**C#**
```csharp
Browser.Zoom.Mode = ZoomMode.PerOrigin;
```

**VB**
```vb
Browser.Zoom.Mode = ZoomMode.PerOrigin
```



## Controlling zoom

You can zoom content of a web page loaded in `IBrowser` programmatically using the `IZoom` 
instance or using touch gestures in the environments with a touch screen.

Zoom level is configured for each host separately. If you set a zoom level for the `http://www.a.com` 
web page, it does not affect the `http://www.b.com` web page.

**Note**
To change the zoom level, you need to 
[wait](https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#loading-url) until the web page is loaded 
completely.


### Zooming in

To zoom in a currently loaded web page, use the following method:


**C#**
```csharp
browser.Zoom.In();
```

**VB**
```vb
browser.Zoom.In()
```



### Zooming out

To zoom out a currently loaded web page, use the following method:


**C#**
```csharp
browser.Zoom.Out();
```

**VB**
```vb
browser.Zoom.Out()
```



### Setting zoom level

The following code sample sets zoom level of the loaded web page to 200%:


**C#**
```csharp
browser.Zoom.Level = Level.P200;
```

**VB**
```vb
browser.Zoom.Level = Level.P200
```



### Resetting the zoom

To reset zoom level to the [default](https://teamdev.com/dotnetbrowser/docs/guides/gs/zoom/#default-zoom-level) 
value, use the code sample below:


**C#**
```csharp
browser.Zoom.Reset();
```

**VB**
```vb
browser.Zoom.Reset()
```



### Disabling the zoom

You can disable zoom for all web pages loaded in the `IBrowser` using the `IZoom.Enabled` property. 
It enables or disables the zoom functionality and resets the zoom level to the default value. After 
that any attempts to change the zoom level programmatically using DotNetBrowser Zoom API and  
touch gestures on a touch screen device are ignored.

For example:


**C#**
```csharp
browser.Zoom.Enabled = false;
```

**VB**
```vb
browser.Zoom.Enabled = False
```



## Zoom events

To get notifications of zoom level change for particular web page, use the `ZoomChanged` event. 
See the code sample below:


**C#**
```csharp
engine.Profiles.Default.ZoomLevels.LevelChanged += (s, e) =>
{
    string hostUrl = e.Host;
    Level zoomLevel = e.Level;
};
```

**VB**
```vb
AddHandler engine.Profiles.Default.ZoomLevels.LevelChanged, Sub(s, e)
    Dim hostUrl As String = e.Host
    Dim zoomLevel As Level = e.Level
End Sub
```


