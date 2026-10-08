# <a id="DotNetBrowser_Zoom_IZoom"></a> Interface IZoom

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

Allows zooming content of a web page.

```csharp
public interface IZoom : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

A <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance belongs to a <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance and can be used only if the
<xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance is alive. When the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance is closed,
<xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance automatically updates its internal state and doesn't allow modifying zoom anymore.
The <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref> will be thrown in this case.

<p></p>

The zoom level is configured for each domain separately, so if you set zoom level for the a.com
web page, it will not be applied for the b.com web page. If you change zoom level
for one domain and then load another one, then the zoom level for another domain will be
default.

## Properties

### <a id="DotNetBrowser_Zoom_IZoom_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Zoom_IZoom_Enabled"></a> Enabled

Enables or disables zoom changes.

```csharp
bool Enabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

By default, zoom functionality
is enabled. You can change zoom level for the currently loaded web page.

<p></p>

To disable zoom functionality, set this property to <code>false</code>. In this case, the browser
instance will revert zoom to the default level, and all attempts to change zoom
will be ignored.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Zoom_IZoom_Level"></a> Level

Gets or sets the zoom level for the currently loaded web page.

```csharp
Level Level { get; set; }
```

#### Property Value

 [Level](DotNetBrowser.Zoom.Level.md)

#### Remarks

Zoom level is configured for each domain separately. For example, if you load the www.a.com web page and
set zoom level to <xref href="DotNetBrowser.Zoom.Level.P250" data-throw-if-not-resolved="false"></xref>, then load the www.b.org web page, the zoom level for
www.b.org web page will be reset to default value. When you load the
www.a.com web page again, its zoom level will be restored
to <xref href="DotNetBrowser.Zoom.Level.P250" data-throw-if-not-resolved="false"></xref> automatically.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Zoom_IZoom_Mode"></a> Mode

Gets or sets how zoom is stored and applied.

```csharp
ZoomMode Mode { get; set; }
```

#### Property Value

 [ZoomMode](DotNetBrowser.Zoom.ZoomMode.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Zoom_IZoom_In"></a> In\(\)

Updates the zoom level for the currently loaded web page on one step up.

```csharp
void In()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Zoom_IZoom_Out"></a> Out\(\)

Updates the zoom level for the currently loaded web page on one step down.

```csharp
void Out()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Zoom_IZoom_Reset"></a> Reset\(\)

Resets the zoom level for the currently loaded web page to default value.

```csharp
void Reset()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

