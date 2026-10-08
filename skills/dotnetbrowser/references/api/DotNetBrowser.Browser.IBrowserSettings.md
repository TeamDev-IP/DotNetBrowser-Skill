# <a id="DotNetBrowser_Browser_IBrowserSettings"></a> Interface IBrowserSettings

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The settings of the browser.

```csharp
public interface IBrowserSettings : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowJavaScriptAccessClipboard"></a> AllowJavaScriptAccessClipboard

Allows or disallows JavaScript code on the web pages loaded in the browser to access clipboard.

```csharp
bool AllowJavaScriptAccessClipboard { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowLoadingImagesAutomatically"></a> AllowLoadingImagesAutomatically

Allows or disallows loading images automatically on the web pages loaded in the browser.

```csharp
bool AllowLoadingImagesAutomatically { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowRunningInsecureContent"></a> AllowRunningInsecureContent

Allows or disallows running an insecure content in the browser.

```csharp
bool AllowRunningInsecureContent { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowScriptsToCloseWindows"></a> AllowScriptsToCloseWindows

Allows or disallows JavaScript code on the web pages loaded in the browser to close the browser.

```csharp
bool AllowScriptsToCloseWindows { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultBackgroundColor"></a> DefaultBackgroundColor

Gets or sets the default browser background color.

```csharp
Color DefaultBackgroundColor { get; set; }
```

#### Property Value

 [Color](DotNetBrowser.Ui.Color.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultEncoding"></a> DefaultEncoding

Gets or sets the default text encoding.

```csharp
string DefaultEncoding { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultFontSize"></a> DefaultFontSize

Gets or sets the default browser font size.

```csharp
FontSize DefaultFontSize { get; set; }
```

#### Property Value

 [FontSize](DotNetBrowser.Ui.FontSize.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultFonts"></a> DefaultFonts

Gets the default fonts used by the browser.

```csharp
IDefaultFonts DefaultFonts { get; }
```

#### Property Value

 [IDefaultFonts](DotNetBrowser.Browser.IDefaultFonts.md)

#### Remarks

The returned object belongs to this browser and can be used while the browser is alive.

### <a id="DotNetBrowser_Browser_IBrowserSettings_ImagesEnabled"></a> ImagesEnabled

Enables or disables images displaying on the web pages loaded in the browser.

```csharp
bool ImagesEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_JavaScriptEnabled"></a> JavaScriptEnabled

Enables or disables JavaScript on the web pages loaded in the browser.

```csharp
bool JavaScriptEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_LocalStorageEnabled"></a> LocalStorageEnabled

Enables or disables the local storage in the browser.

```csharp
bool LocalStorageEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_OverscrollHistoryNavigationEnabled"></a> OverscrollHistoryNavigationEnabled

Enables or disables the back/forward navigation with a left/right swipe in the browser.

```csharp
bool OverscrollHistoryNavigationEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_PluginsEnabled"></a> PluginsEnabled

Enables or disables plugins on the web pages loaded in the browser.

```csharp
bool PluginsEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_PreferredColorScheme"></a> PreferredColorScheme

Gets or sets the preferred color scheme for the web content in the browser.

```csharp
PreferredColorScheme PreferredColorScheme { get; set; }
```

#### Property Value

 [PreferredColorScheme](DotNetBrowser.Browser.PreferredColorScheme.md)

#### Remarks

The scheme is used to evaluate the <code>prefers-color-scheme</code> media query and resolve UA color scheme to be used
based on the <code>supported-color-schemes</code> META tag and CSS property.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_ScrollbarsHidden"></a> ScrollbarsHidden

Hides or shows scrollbars on the web pages.

```csharp
bool ScrollbarsHidden { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_TransparentBackgroundEnabled"></a> TransparentBackgroundEnabled

Enables or disables transparent background on the web pages.By default, the background is always
opaque.

```csharp
bool TransparentBackgroundEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    This property supports only the <xref href="DotNetBrowser.Engine.RenderingMode.OffScreen" data-throw-if-not-resolved="false"></xref> rendering mode
    on Windows and Linux, and the both rendering modes on macOS.
</p>
<p>
    The attempt to set this property to <code>true</code> in the unsupported rendering mode will result in an
    exception.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowserSettings_WebRtcIpHandlingPolicy"></a> WebRtcIpHandlingPolicy

Gets or sets the WebRTC IP handling policy for the browser.

```csharp
WebRtcIpHandlingPolicy WebRtcIpHandlingPolicy { get; set; }
```

#### Property Value

 [WebRtcIpHandlingPolicy](DotNetBrowser.Browser.WebRtcIpHandlingPolicy.md)

#### Remarks

Specifying the custom WebRTC IP handling policy can be used to protect against WebRTC leaks - the WebRTC itself
will remain enabled.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

