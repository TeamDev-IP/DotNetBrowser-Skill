
# Plugins

**Lead**
DotNetBrowser supports Chromium plugins. This guide describes how to get the information about all the installed and available Chromium plugins, enable or disable a specified plugin on a web page, and other actions.


Use `IPlugins` to get information about all the available plugins and enable/disable plugins on a web page. By default, all plugins are enabled.

Plugins are associated with [`Profiles`](https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/). If you want to obtain the `Plugins` service for a specific `Profile`, use the `Profile.Plugins` property. To access the `Plugins` service for the default profile, use `engine.Profiles.Default.Plugins`.

**Note**
By default all plugins are enabled.


## Installed plugins

To get the information about all the installed and available plugins, use the code sample below:


**C#**
```csharp
foreach (Plugin plugin in engine.Profiles.Default.Plugins.AvailablePlugins)
{
    string name = plugin.Name;
    string description = plugin.Description;
    string version = plugin.Version;
}
```

**VB**
```vb
For Each plugin As Plugin In engine.Profiles.Default.Plugins.AvailablePlugins
    Dim name As String = plugin.Name
    Dim description As String = plugin.Description
    Dim version As String = plugin.Version
Next
```



## Filtering plugins

Every time when a web page needs to access a plugin, the `AllowPluginHandler` is used. In this handler, you can instruct the web page whether the requested plugin is allowed.

The following example demonstrates how to deny all plugins with the `application/pdf` MIME type:


**C#**
```csharp
engine.Profiles.Default.Plugins.AllowPluginHandler = 
    new Handler<AllowPluginParameters, AllowPluginResponse>(p =>
    { 
        // Get plugin MIME types.
        IEnumerable<MimeType> pluginMimeTypes = p.Plugin.MimeTypes;
        // Deny all plugins with the "application/pdf" MIME type.
        if (pluginMimeTypes.Contains(MimeType.ApplicationPdf))
        {
            return AllowPluginResponse.Deny();
        }
        return AllowPluginResponse.Allow();
    });
```

**VB**
```vb
engine.Profiles.Default.Plugins.AllowPluginHandler = 
    New Handler(Of AllowPluginParameters, AllowPluginResponse)(Function(p)
        ' Get plugin MIME types.
        Dim pluginMimeTypes As IEnumerable(Of MimeType) = p.Plugin.MimeTypes
        ' Deny all plugins with the "application/pdf" MIME type.
        If pluginMimeTypes.Contains(MimeType.ApplicationPdf) Then
            Return AllowPluginResponse.Deny()
        End If
        Return AllowPluginResponse.Allow()
    End Function)
```



## PDF

DotNetBrowser supports the built-in Chromium PDF Viewer plugin. You can display a PDF file available on a remote web server using URL of the PDF file, or a PDF file located in your local file system:

![Chromium PDF Viewer](https://teamdev.com/dotnetbrowser/img/articles/guides/plugins/pdf-viewer.webp)

### PDF viewer toolbar

By default, PDF Viewer displays the built-in controls such as zoom buttons, toolbar with the file name, page number, **Rotate**, **Download**, and **Print** buttons. You can hide these controls by adding `#toolbar=0` to the end of the URL.

For example, `http://www.orimi.com/pdf-test.pdf#toolbar=0`

For PDFs loaded from the local file system, use the following URL format: 

`file:///D:/Downloads/pdf-test.pdf#toolbar=0`

![No Toolbar](https://teamdev.com/dotnetbrowser/img/articles/guides/plugins/no-toolbar.webp)

### Disabling PDF viewer

By default, the PDF files will be displayed in the PDF Viewer. To download the PDFs instead of displaying them, use the `IBrowserSettings.PdfViewerEnabled` property:


**C#**
```csharp
engine.Profiles.Default.Plugins.Settings.PdfViewerEnabled = false;
```

**VB**
```vb
engine.Profiles.Default.Plugins.Settings.PdfViewerEnabled = False
```



### Password-protected PDF

By default, the standard Chromium dialog is shown when the encrypted PDF is loaded:

![Encrypted PDF](https://teamdev.com/dotnetbrowser/img/articles/guides/plugins/encrypted-pdf.webp)

To provide password programmatically, use `RequestPdfDocumentPasswordHandler`:


**C#**
```csharp
// Provide the password programmatically.
Browser.RequestPdfDocumentPasswordHandler =
    new Handler<RequestPdfDocumentPasswordParameters, RequestPdfDocumentPasswordResponse>(p
        => RequestPdfDocumentPasswordResponse.Password(Password));
```

**VB**
```vb
' Provide the password programmatically.
Browser.RequestPdfDocumentPasswordHandler = 
    New Handler(Of RequestPdfDocumentPasswordParameters, 
        RequestPdfDocumentPasswordResponse)(Function(p) 
            RequestPdfDocumentPasswordResponse.Password(Password))
```




## Adobe Flash

**Important**
[Adobe Flash reaches its end-of-life](https://blog.adobe.com/en/publish/2017/07/25/adobe-flash-update) in December 2020. The versions of DotNetBrowser based on Chromium 87 and below may still work with Flash if the corresponding plugin is installed and configured in the system.


Since version 88, Chromium does not support Flash. DotNetBrowser does not support it as well starting from version 2.5.

## NPAPI plugins

Since version 49, Chromium does not support any of NPAPI plugins, including **Microsoft Silverlight**, DotNetBrowser does not support them as well.

## ActiveX

Since ActiveX is not supported by Chromium, DotNetBrowser does not support it as well.
