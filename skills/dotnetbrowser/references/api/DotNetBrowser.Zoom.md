# <a id="DotNetBrowser_Zoom"></a> Namespace DotNetBrowser.Zoom

### Namespaces

 [DotNetBrowser.Zoom.Events](DotNetBrowser.Zoom.Events.md)

### Classes

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

A zoom level of a web page. Provides a set of the pre-defined constants. Each constant name
consists of the <code>P</code> prefix followed by a number. The number represents a zoom level in
percents. For example, the <xref href="DotNetBrowser.Zoom.Level.P25" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Zoom.Level.P110" data-throw-if-not-resolved="false"></xref> values represent the 25% and 110% zoom
levels accordingly.

### Interfaces

 [IZoom](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_IZoom)

Allows zooming content of a web page.

 [IZoomLevels](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_IZoomLevels)

Allows configuring the default zoom levels and receive notifications about zoom changes.

### Enums

 [ZoomMode](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_ZoomMode)

Defines how zoom settings are stored and applied.

## <a id="DotNetBrowser_Zoom_Level"></a> Class Level

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

A zoom level of a web page. Provides a set of the pre-defined constants. Each constant name
consists of the <code>P</code> prefix followed by a number. The number represents a zoom level in
percents. For example, the <xref href="DotNetBrowser.Zoom.Level.P25" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Zoom.Level.P110" data-throw-if-not-resolved="false"></xref> values represent the 25% and 110% zoom
levels accordingly.

```csharp
public sealed class Level : TypedEnum<double>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<double\> ← 
[Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Zoom_Level_P100"></a> P100

100% (default zoom level)

```csharp
public static readonly Level P100
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P110"></a> P110

110%

```csharp
public static readonly Level P110
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P125"></a> P125

125%

```csharp
public static readonly Level P125
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P150"></a> P150

150%

```csharp
public static readonly Level P150
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P175"></a> P175

175%

```csharp
public static readonly Level P175
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P200"></a> P200

200%

```csharp
public static readonly Level P200
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P25"></a> P25

25%

```csharp
public static readonly Level P25
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P250"></a> P250

250%

```csharp
public static readonly Level P250
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P300"></a> P300

300%

```csharp
public static readonly Level P300
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P33"></a> P33

33%

```csharp
public static readonly Level P33
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P400"></a> P400

400%

```csharp
public static readonly Level P400
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P50"></a> P50

50%

```csharp
public static readonly Level P50
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P500"></a> P500

500%

```csharp
public static readonly Level P500
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P67"></a> P67

67%

```csharp
public static readonly Level P67
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P75"></a> P75

75%

```csharp
public static readonly Level P75
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P80"></a> P80

80%

```csharp
public static readonly Level P80
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

#### <a id="DotNetBrowser_Zoom_Level_P90"></a> P90

90%

```csharp
public static readonly Level P90
```

##### Field Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

### Methods

#### <a id="DotNetBrowser_Zoom_Level_Create_System_Double_"></a> Create\(double\)

Initializes a new <xref href="DotNetBrowser.Zoom.Level" data-throw-if-not-resolved="false"></xref> instance from its double representation.

```csharp
public static Level Create(double value)
```

##### Parameters

`value` [double](https://learn.microsoft.com/dotnet/api/system.double)

The level representation.

##### Returns

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

The initialized <xref href="DotNetBrowser.Zoom.Level" data-throw-if-not-resolved="false"></xref> instance.

### Operators

#### <a id="DotNetBrowser_Zoom_Level_op_Explicit_System_Double__DotNetBrowser_Zoom_Level"></a> explicit operator Level\(double\)

Initializes a new <xref href="DotNetBrowser.Zoom.Level" data-throw-if-not-resolved="false"></xref> instance from its double representation.

```csharp
public static explicit operator Level(double value)
```

##### Parameters

`value` [double](https://learn.microsoft.com/dotnet/api/system.double)

The level representation.

##### Returns

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

The initialized <xref href="DotNetBrowser.Zoom.Level" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Zoom_IZoom"></a> Interface IZoom

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

Allows zooming content of a web page.

```csharp
public interface IZoom : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

A <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance belongs to a <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance and can be used only if the
<xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance is alive. When the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance is closed,
<xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance automatically updates its internal state and doesn't allow modifying zoom anymore.
The <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref> will be thrown in this case.

<p></p>

The zoom level is configured for each domain separately, so if you set zoom level for the a.com
web page, it will not be applied for the b.com web page. If you change zoom level
for one domain and then load another one, then the zoom level for another domain will be
default.

### Properties

#### <a id="DotNetBrowser_Zoom_IZoom_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Zoom_IZoom_Enabled"></a> Enabled

Enables or disables zoom changes.

```csharp
bool Enabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

By default, zoom functionality
is enabled. You can change zoom level for the currently loaded web page.

<p></p>

To disable zoom functionality, set this property to <code>false</code>. In this case, the browser
instance will revert zoom to the default level, and all attempts to change zoom
will be ignored.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Zoom_IZoom_Level"></a> Level

Gets or sets the zoom level for the currently loaded web page.

```csharp
Level Level { get; set; }
```

##### Property Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

##### Remarks

Zoom level is configured for each domain separately. For example, if you load the www.a.com web page and
set zoom level to <xref href="DotNetBrowser.Zoom.Level.P250" data-throw-if-not-resolved="false"></xref>, then load the www.b.org web page, the zoom level for
www.b.org web page will be reset to default value. When you load the
www.a.com web page again, its zoom level will be restored
to <xref href="DotNetBrowser.Zoom.Level.P250" data-throw-if-not-resolved="false"></xref> automatically.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Zoom_IZoom_Mode"></a> Mode

Gets or sets how zoom is stored and applied.

```csharp
ZoomMode Mode { get; set; }
```

##### Property Value

 [ZoomMode](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_ZoomMode)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Zoom_IZoom_In"></a> In\(\)

Updates the zoom level for the currently loaded web page on one step up.

```csharp
void In()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Zoom_IZoom_Out"></a> Out\(\)

Updates the zoom level for the currently loaded web page on one step down.

```csharp
void Out()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Zoom_IZoom_Reset"></a> Reset\(\)

Resets the zoom level for the currently loaded web page to default value.

```csharp
void Reset()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Zoom_IZoomLevels"></a> Interface IZoomLevels

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the default zoom levels and receive notifications about zoom changes.

```csharp
public interface IZoomLevels : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Zoom_IZoomLevels_DefaultLevel"></a> DefaultLevel

Gets or sets the default zoom level for pages that don't override it.

```csharp
Level DefaultLevel { get; set; }
```

##### Property Value

 [Level](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_Level)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoomLevels" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Zoom_IZoomLevels_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Zoom_IZoomLevels_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Zoom_IZoomLevels_LevelChanged"></a> LevelChanged

Occurs when the zoom level for a specific URL has been changed.

```csharp
event EventHandler<LevelChangedEventArgs> LevelChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[LevelChangedEventArgs](DotNetBrowser.Zoom.Events.md#DotNetBrowser_Zoom_Events_LevelChangedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Zoom.IZoomLevels" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Zoom_ZoomMode"></a> Enum ZoomMode

Namespace: [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)  
Assembly: DotNetBrowser.dll  

Defines how zoom settings are stored and applied.

```csharp
public enum ZoomMode
```

### Fields

`PerBrowser = 2` 

Stores zoom level per browser instance.



`PerOrigin = 1` 

Stores zoom level per origin.
