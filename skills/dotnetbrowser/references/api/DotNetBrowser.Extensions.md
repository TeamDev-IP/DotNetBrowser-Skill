# <a id="DotNetBrowser_Extensions"></a> Namespace DotNetBrowser.Extensions

### Namespaces

 [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)

 [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)

### Classes

 [ExtensionInstallationException](DotNetBrowser.Extensions.ExtensionInstallationException.md)

Thrown when the extension installation has failed for some reason.

### Interfaces

 [IExtension](DotNetBrowser.Extensions.IExtension.md)

A Chromium extension.

<p>
    Extensions can be installed via the <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> instance. It's possible
    to install an extension either from the CRX file or from the Chrome WebStore. Each extension
    is installed on a per-profile basis, and is not shared with other profiles.
</p>

 [IExtensionAction](DotNetBrowser.Extensions.IExtensionAction.md)

The extension action is a clickable extension icon.

<p></p>

In Chrome, extension actions are located in the top-right corner of the toolbar.
Clicking the icon usually results in showing an extension action popup. If the extension
requests to show a popup, the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref> is invoked.
The extension can also handle the click action without showing any popups, in which case
the handler is not invoked.

 [IExtensions](DotNetBrowser.Extensions.IExtensions.md)

A service that allows managing extensions.

### Enums

 [ExtensionActionType](DotNetBrowser.Extensions.ExtensionActionType.md)

The extension action type.

 [ExtensionPermission](DotNetBrowser.Extensions.ExtensionPermission.md)

The extension permission types.

