
# Chrome Extensions

**Lead**
This page describes how to work with Chrome extensions.


**Note**
The functionality described in this article is available in DotNetBrowser 3.0.0 or higher.


DotNetBrowser provides the Extensions API that allows you to install, update, and uninstall Chrome extensions. The
extensions work on a per-profile basis and are not shared with other profiles. To access the extensions of a specific
profile, use the following approach:


**C#**
```csharp
IExtensions extensions = profile.Extensions;
```

**VB**
```vb
Dim extensions As IExtensions = profile.Extensions
```



If you delete the profile, all installed extensions for this profile will be deleted as well.

## Installing extensions

You can install Chrome extensions manually from [Chrome Web Store](https://chromewebstore.google.com/) or programmatically from CRX files.

We recommend that you install extensions from CRX files if you trust the source of the extension. Comparing to
installing extensions from Chrome Web Store, it gives you the following benefits:

1. You control the version of the extension that you install. You can test the extension with a specific DotNetBrowser
   version and make sure that it works as expected with the Chromium build that DotNetBrowser uses. If you install the
   extension from Chrome Web Store, you install the latest version of the extension that may not be compatible with the
   DotNetBrowser version you use.
2. You can deploy the extension with your application and install it automatically. So, you don't need to ask users to
   install the extension manually from Chrome Web Store.
3. You can install extensions that are not available in Chrome Web Store. If you develop an extension you would like to
   use in DotNetBrowser and you don't want to publish it in Chrome Web Store, you can pack it into a CRX file and use it.

To install an extension from a CRX file, use the following approach:


**C#**
```csharp
string crxPath = Path.GetFullPath("path/to/extension.crx");
IExtension extension = await extensions.Install(crxPath);
```

**VB**
```vb
Dim crxPath As String = Path.GetFullPath("path/to/extension.crx")
Dim extension As IExtension = Await extensions.Install(crxPath)
```



The method returns an instance of the installed extension. All the required permissions required by the extension are
automatically granted.

**Note**
**Important**: Be very cautious about the extensions you are installing. In Chrome Web Store, the CRX file must have publisher proof, which is obtained upon extension publishing. In DotNetBrowser, we allow users to install the extensions without publisher proof, so be cautious about the resources you use to obtain CRX files.


Installing extensions from Chrome Web Store is disabled by default for security reasons. If you want to let users
install extensions from Chrome Web Store, you need to allow installation using the following approach:


**C#**
```csharp
extensions.InstallExtensionHandler =
    new Handler<InstallExtensionParameters, InstallExtensionResponse>(p => 
        InstallExtensionResponse.Install);
```

**VB**
```vb
extensions.InstallExtensionHandler = 
    New Handler(Of InstallExtensionParameters, InstallExtensionResponse)(
        Function(p) InstallExtensionResponse.Install)
```



Every time the user clicks the "Add to Chrome" button on the Chrome Web Store page, the `InstallExtensionHandler` will be invoked. You can get info about the extension that the user wants to install from the `InstallExtensionParameters` object
and decide whether to allow the installation or not:


**C#**
```csharp
extensions.InstallExtensionHandler =
    new Handler<InstallExtensionParameters, InstallExtensionResponse>(p => 
    {
        string name = p.ExtensionName;
        string version = p.ExtensionVersion;
        if (name.Equals("uBlock Origin") && version.Equals("1.35.2")) 
        {
            return InstallExtensionResponse.Install;
        } 
        else 
        {
            return InstallExtensionResponse.Cancel;
        }
    });
```

**VB**
```vb
extensions.InstallExtensionHandler =
    New Handler(Of InstallExtensionParameters, InstallExtensionResponse)(
        Function(p)
            Dim name As String = p.ExtensionName
            Dim version As String = p.ExtensionVersion
            If name.Equals("uBlock Origin") AndAlso version.Equals("1.35.2") Then
                Return InstallExtensionResponse.Install
            Else
                Return InstallExtensionResponse.Cancel
            End If
        End Function)
```



To get notified when the extension is installed, use the `ExtensionInstalled` event:


**C#**
```csharp
extensions.ExtensionInstalled += (s, e) => 
{
    IExtension installedExtension = e.Extension;
};
```

**VB**
```vb
AddHandler extensions.ExtensionInstalled, Sub(s, e)
    Dim installedExtension As IExtension = e.Extension
End Sub
```



## Updating extensions

If you install an extension from a CRX file, and you would like to update it with a new version, you just need to
install it from a new CRX file:


**C#**
```csharp
string updatedCrxPath = Path.GetFullPath("path/to/updated_extension.crx");
IExtension extension = await extensions.Install(updatedCrxPath);
```

**VB**
```vb
Dim updatedCrxPath As String = Path.GetFullPath("path/to/updated_extension.crx")
Dim extension As IExtension = Await extensions.Install(updatedCrxPath)
```



You don't need to delete the previous version of the extension. DotNetBrowser will automatically update the extension to the
newest version.

**Note**
**Important**: When you are installing an extension without publisher proof, be sure to use the same private key (`.pem` file) for packaging. When a different private key is used or not used at all, the extension would be considered as new and would be installed again without updating.


If you install an extension from Chrome Web Store, you can't update it programmatically. The user should update the
extension manually from the extension page in Chrome Web Store.

To get notified when the extension is updated, use the `ExtensionUpdated` event:


**C#**
```csharp
extensions.ExtensionUpdated += (s, e) => 
{
    IExtension updatedExtension = e.Extension;
};
```

**VB**
```vb
AddHandler extensions.ExtensionUpdated, Sub(s, e)
    Dim updatedExtension As IExtension = e.Extension
End Sub
```



## Uninstalling extensions

You can programmatically uninstall the extension you installed from a CRX file or Chrome Web Store:


**C#**
```csharp
IExtension extension = 
    extensions.All.FirstOrDefault(ex => ex.Name.Equals("uBlock Origin"));
await extension.Uninstall();
```

**VB**
```vb
Dim extension As IExtension = 
        extensions.All.FirstOrDefault(
            Function(ex) ex.Name.Equals("uBlock Origin"))
Await extension.Uninstall()
```



If the extension was installed manually from Chrome Web Store, the user might want to uninstall it manually as well. By
default, uninstalling extensions from Chrome Web Store is disabled for security reasons. If you want to allow users to
uninstall extensions from Chrome Web Store or the chrome://extensions page, you need to allow uninstallation:


**C#**
```csharp
extensions.UninstallExtensionHandler =
    new Handler<UninstallExtensionParameters, UninstallExtensionResponse>(p => 
        UninstallExtensionResponse.Uninstall);
```

**VB**
```vb
extensions.UninstallExtensionHandler = 
    New Handler(Of UninstallExtensionParameters, UninstallExtensionResponse)(
        Function(p) UninstallExtensionResponse.Uninstall)
```



To get notified when the extension is uninstalled, use the `ExtensionUninstalled` event:


**C#**
```csharp
extensions.ExtensionUninstalled += (s, e) => 
{
    string extensionId = e.ExtensionId;
};
```

**VB**
```vb
AddHandler extensions.ExtensionUninstalled, Sub(s, e)
    Dim extensionId As String = e.ExtensionId
End Sub
```



An attempt to work with an uninstalled extension will result in an `ObjectDisposedException`.

## Extension action

Chrome extensions may provide features that are available only in the "extension action popup". This is a dialog
that you see when clicking on the extension icon in the Chrome toolbar. Even though DotNetBrowser does not display Chrome 
toolbar. Instead, it provides an API for interacting with the extension action popup.

To simulate the click on the extension icon (extension action) in Chrome toolbar for a specific tab, execute the
following code:


**C#**
```csharp
extension.GetAction(browser)?.Click();
```

**VB**
```vb
If extension.GetAction(browser) IsNot Nothing Then
    extension.GetAction(browser).Click()
End If
```



**Note**
An extension, not Chromium, is responsible for picking a browser to interact with. Therefore, the extension action may not be executed for the `browser` it was obtained for.


If you want to display the extension icon in your application, you can access the extension action properties and subscribe to the action update notifications:


**C#**
```csharp
IExtensionAction action = extension.GetAction(browser);

if (action != null) 
{
    // Get the properties of the action.
    Bitmap icon = action.Icon;
    string badge = action.Badge;
    string tooltip = action.Tooltip;
    bool enabled = action.IsEnabled;

    // Get notifications when the extension action is updated.
    action.Updated += (s, e) => 
    {
        IExtensionAction updatedAction = e.ExtensionAction;
    };
}
```

**VB**
```vb
Dim action As IExtensionAction = extension.GetAction(browser)

If action IsNot Nothing Then
    ' Get the properties of the action.
    Dim icon As Bitmap = action.Icon
    Dim badge As String = action.Badge
    Dim tooltip As String = action.Tooltip
    Dim enabled As Boolean = action.IsEnabled

    ' Get notifications when the extension action is updated.
    AddHandler action.Updated, Sub(s, e)
        Dim updatedAction As IExtensionAction = e.ExtensionAction
    End Sub
End If
```



## Extension action popups

When you create a `BrowserView` instance, it will register the default implementations of the `OpenExtensionActionPopupHandler` callback that will display the extension action popup when the program simulates the click on the extension action icon.

If you want to display a custom extension action popup, register your own implementation of
the `OpenExtensionActionPopupHandler`:


**C#**
```csharp
Browser.OpenExtensionActionPopupHandler = 
    new Handler<OpenExtensionActionPopupParameters>(p =>
    {
        IBrowser popupBrowser = p.PopupBrowser;
    });
```

**VB**
```vb
Browser.OpenExtensionActionPopupHandler =
    New Handler(Of OpenExtensionActionPopupParameters)(
        Sub(p)
            Dim popupBrowser As IBrowser = p.PopupBrowser
        End Sub)
```



## Extension popups

Some extensions may want to open popup windows to show a website or some other content. By default,
DotNetBrowser blocks such popups. To allow the extension to show popups, register your own implementation of the following callbacks:


**C#**
```csharp
extension.OpenExtensionPopupHandler = 
    new Handler<OpenExtensionPopupParameters>(p =>
    {
        IBrowser popupBrowser = p.PopupBrowser;
    });
```

**VB**
```vb
extension.OpenExtensionPopupHandler =
    New Handler(Of OpenExtensionPopupParameters)(
        Sub(p)
            Dim popupBrowser As IBrowser = p.PopupBrowser
        End Sub)
```



Or use the default implementation:


**C#**
```csharp
extension.OpenExtensionPopupHandler = new DefaultOpenExtensionPopupHandler(browserView);
```

**VB**
```vb
extension.OpenExtensionPopupHandler = New DefaultOpenExtensionPopupHandler(browserView)
```



**Note**
Please note that "extension popups" and "extension action popups" are different things.


## Peculiarities & limitations

We designed extension API with the goal to behave as Chromium as much as possible. But since DotNetBrowser is an embedded
browser, we can't ensure the same behavior for every case. Thus, there are peculiarities and limitations that you should
have in mind when working with extensions.

1. All tabs are opened as new windows.
2. `chrome.tabs.query` never takes into account extension action popups.
3. Windows of the extension action popup are auto-resizable. The size is regulated by the extension action.
4. When DotNetBrowser does not find the manifest for native messaging (`chrome.runtime.connectNative`) in the user data
   directory or Chromium application data, it checks it in Chrome application data.

There are certain limitations related to Chromium tabs, windows, and other UI elements. The `windows.Window` is mapped
to a native window associated with the browser, not the .NET window it is embedded into (if any). Thus, methods and
properties of the `windows.Window` object, such as `Window.width`, `Window.height`, `Window.focused`, etc., are bound to
that native window.

### Unsupported extensions APIs

Below is the list of Chromium Extension APIs that are not supported in DotNetBrowser:

* `chrome.tabs.discard`
* `chrome.tabs.remove`
* `chrome.tabs.duplicate`
* `chrome.windows.remove`
* `chrome.windows.update`
* `chrome.window.create` with more than one URL in parameters
* `chrome.sessions.restore`
* `chrome.desktopCapture.chooseDesktopMedia`.

If an extension calls an unsupported method that returns a `Promise`, it will be rejected with an error. If a method
accepts a callback, the `chrome.runtime.lastError` property will be set to an error.

## Downloading CRX from Chrome Web Store

If you want to download a CRX file of an extension available in Chrome Web Store, then you can register
the `InstallExtensionCallback` callback where you can get an absolute path to the CRX file of the extension that is
about to be installed from Chrome Web Store and make a copy of it to a different location:


**C#**
```csharp
extensions.InstallExtensionHandler =
    new Handler<InstallExtensionParameters, InstallExtensionResponse>(p =>
    {
        string name = p.ExtensionName;
        string version = p.ExtensionVersion;
        string sourceCrxFilePath = Path.GetFullPath(p.ExtensionCrxFile);
        string targetCrxFilePath = Path.GetFullPath(name + "-" + version + ".crx");
        try
        {
            File.Copy(sourceCrxFilePath, targetCrxFilePath);
        }
        catch (IOException e)
        {
            throw new InvalidOperationException(e.Message, e);
        }
        return InstallExtensionResponse.Cancel;
    });
```

**VB**
```vb
extensions.InstallExtensionHandler =
    New Handler(Of InstallExtensionParameters, InstallExtensionResponse)(
        Function(p)
            Dim name As String = p.ExtensionName
            Dim version As String = p.ExtensionVersion
            Dim sourceCrxFilePath As String = Path.GetFullPath(p.ExtensionCrxFile)
            Dim targetCrxFilePath As String = Path.GetFullPath(name & "-" & version & ".crx")
            Try
                File.Copy(sourceCrxFilePath, targetCrxFilePath)
            Catch e As IOException
                Throw New InvalidOperationException(e.Message, e)
            End Try
            Return InstallExtensionResponse.Cancel
        End Function)
```



Now, you can load the required extension in Chrome Web Store and click the "Add to Chrome" button. The callback will be
invoked, and the CRX file of the extension will be copied to the specified location.