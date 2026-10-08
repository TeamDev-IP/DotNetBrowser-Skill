# <a id="DotNetBrowser_Plugins_IPluginSettings"></a> Interface IPluginSettings

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The settings to configure the available Chromium <xref href="DotNetBrowser.Plugins" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IPluginSettings : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Plugins_IPluginSettings_PdfViewerEnabled"></a> PdfViewerEnabled

Enables or disables the built-in PDF viewer.

```csharp
bool PdfViewerEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    This setting controls how DotNetBrowser handles navigations to web pages
    embedding PDF documents. When the PDF viewer is enabled,
    then the PDF document will be displayed in the PDF viewer. Otherwise, the engine
    will download the PDF document, like any other resource that cannot be rendered in the
    browser. The download can be configured via the <xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    Changing this setting affects only subsequent navigations and does not affect the
    already loaded web pages.
</p>
<p>
    By default, the PDF viewer is enabled.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPluginSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

