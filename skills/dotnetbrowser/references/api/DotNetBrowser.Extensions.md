# <a id="DotNetBrowser_Extensions"></a> Namespace DotNetBrowser.Extensions

### Namespaces

 [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)

 [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)

### Classes

 [ExtensionInstallationException](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionInstallationException)

Thrown when the extension installation has failed for some reason.

### Interfaces

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

A Chromium extension.

<p>
    Extensions can be installed via the <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> instance. It's possible
    to install an extension either from the CRX file or from the Chrome WebStore. Each extension
    is installed on a per-profile basis, and is not shared with other profiles.
</p>

 [IExtensionAction](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensionAction)

The extension action is a clickable extension icon.

<p></p>

In Chrome, extension actions are located in the top-right corner of the toolbar.
Clicking the icon usually results in showing an extension action popup. If the extension
requests to show a popup, the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref> is invoked.
The extension can also handle the click action without showing any popups, in which case
the handler is not invoked.

 [IExtensions](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensions)

A service that allows managing extensions.

### Enums

 [ExtensionActionType](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionActionType)

The extension action type.

 [ExtensionPermission](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionPermission)

The extension permission types.

## <a id="DotNetBrowser_Extensions_ExtensionInstallationException"></a> Class ExtensionInstallationException

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

Thrown when the extension installation has failed for some reason.

```csharp
public class ExtensionInstallationException : InvalidOperationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[SystemException](https://learn.microsoft.com/dotnet/api/system.systemexception) ← 
[InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception) ← 
[ExtensionInstallationException](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionInstallationException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[Exception.SerializeObjectState](https://learn.microsoft.com/dotnet/api/system.exception.serializeobjectstate), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Extensions_ExtensionInstallationException__ctor_System_String_"></a> ExtensionInstallationException\(string\)

```csharp
public ExtensionInstallationException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Extensions_IExtension"></a> Interface IExtension

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

A Chromium extension.

<p>
    Extensions can be installed via the <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> instance. It's possible
    to install an extension either from the CRX file or from the Chrome WebStore. Each extension
    is installed on a per-profile basis, and is not shared with other profiles.
</p>

```csharp
public interface IExtension : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

<p>
    There are certain limitations related to Chromium tabs, windows, and other UI elements.
    The
    <a href="https://developer.chrome.com/docs/extensions/reference/windows/#type-Window">
        <code>windows.Window</code>
    </a>
    Extensions API object is mapped to a native window associated with the browser,
    not the .NET window it is embedded into. Thus, methods and properties of the <code>windows.Window</code> object,
    such as <code>Window.width</code>, <code>Window.height</code>, <code>Window.focused</code>, etc. are bound
    to that native window.
</p>
<p>
    From Chromium's perspective, each browser is a window with one tab. Extensions that manipulate
    tabs, tab groups, or windows should be used with caution, as they might not work as expected.
</p>
<p>
    Below is the list of Chromium Extension APIs that are not supported in DotNetBrowser:

<ul><li><code>chrome.tabs.discard</code>,</li><li><code>chrome.tabs.remove</code>,</li><li><code>chrome.tabs.duplicate</code>,</li><li><code>chrome.windows.remove</code>,</li><li><code>chrome.windows.update</code>,</li><li><code>chrome.window.create</code>  with more than one URL in parameters,</li><li><code>chrome.sessions.restore</code>,</li><li><code>chrome.downloads.*</code>,</li><li><code>chrome.desktopCapture.chooseDesktopMedia</code>.</li></ul>
</p>
<p>
    If an extension calls an unsupported method that returns a <code>Promise</code>, it will be
    rejected with an error. If a method accepts a callback, the <code>chrome.runtime.lastError</code>
    property will be set to an error.
</p>

### Properties

#### <a id="DotNetBrowser_Extensions_IExtension_HasAction"></a> HasAction

Indicates whether an extension has an action.

```csharp
bool HasAction { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtension_Id"></a> Id

Gets the identifier of the extension.

```csharp
string Id { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtension_Name"></a> Name

Gets the name of the extension.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtension_OpenExtensionPopupHandler"></a> OpenExtensionPopupHandler

Gets or sets a handler that is used when the extension is about to open a popup window.

```csharp
IHandler<OpenExtensionPopupParameters> OpenExtensionPopupHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters)\>

##### Remarks

The callback is invoked by the following extension API functions:

<ul><li><code>chrome.tabs.create</code>,</li><li><code>chrome.windows.create</code>,</li><li><code>chrome.runtime.openOptionsPage</code>,</li><li><code>setUninstallURL</code>, upon uninstalling an extension.</li></ul>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtension_Profile"></a> Profile

Gets the profile instance associated with this extension.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

### Methods

#### <a id="DotNetBrowser_Extensions_IExtension_GetAction_DotNetBrowser_Browser_IBrowser_"></a> GetAction\(IBrowser\)

Gets the extension action for the given <code class="paramref">browser</code>.

```csharp
IExtensionAction GetAction(IBrowser browser)
```

##### Parameters

`browser` [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

The browser that will be associated with the action.

##### Returns

 [IExtensionAction](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensionAction)

The extension action for the passed browser or <code>null</code> if the action is not available.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtension_Uninstall"></a> Uninstall\(\)

Uninstalls this extension.

```csharp
Task<bool> Uninstall()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

A task that completes when the extension is uninstalled. The result value is <code>true</code> if the extension was
uninstalled successfully, <code>false</code> otherwise.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Extensions_IExtensionAction"></a> Interface IExtensionAction

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

The extension action is a clickable extension icon.

<p></p>

In Chrome, extension actions are located in the top-right corner of the toolbar.
Clicking the icon usually results in showing an extension action popup. If the extension
requests to show a popup, the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref> is invoked.
The extension can also handle the click action without showing any popups, in which case
the handler is not invoked.

```csharp
public interface IExtensionAction : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Badge"></a> Badge

Gets the extension action badge text for the given browser.

```csharp
string Badge { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Browser"></a> Browser

Gets the browser instance associated with this extension action.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Extension"></a> Extension

Gets the extension associated with this extension action.

```csharp
IExtension Extension { get; }
```

##### Property Value

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Icon"></a> Icon

Gets the extension action icon for the given browser.

```csharp
Bitmap Icon { get; }
```

##### Property Value

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensionAction_IsEnabled"></a> IsEnabled

Indicates whether the extension action is currently enabled.

```csharp
bool IsEnabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Tooltip"></a> Tooltip

Gets the extension action tooltip.

```csharp
string Tooltip { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Type"></a> Type

Gets the extension action type.

```csharp
ExtensionActionType Type { get; }
```

##### Property Value

 [ExtensionActionType](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionActionType)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

### Methods

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Click"></a> Click\(\)

Simulates a click on the extension action icon for the given browser.

```csharp
void Click()
```

##### Remarks

Clicking a disabled action is no-op.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensionAction_Updated"></a> Updated

Occurs when the extension action has been updated.

```csharp
event EventHandler<ExtensionActionUpdatedEventArgs> Updated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionActionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs)\>

##### Remarks

You can use this event to monitor changes in the extension action badge, tooltip, or icon.

## <a id="DotNetBrowser_Extensions_IExtensions"></a> Interface IExtensions

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing extensions.

```csharp
public interface IExtensions : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Extensions_IExtensions_All"></a> All

Gets all extensions that are currently installed for the profile.

```csharp
IReadOnlyCollection<IExtension> All { get; }
```

##### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensions_InstallExtensionHandler"></a> InstallExtensionHandler

Gets or sets a handler that is used when the user installs an extension from Chrome Web Store.

```csharp
IHandler<InstallExtensionParameters, InstallExtensionResponse> InstallExtensionHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[InstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionParameters), [InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionResponse)\>

##### Remarks

<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Install" data-throw-if-not-resolved="false"></xref> value to install the extension.</p>
<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> value to cancel the installation.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Extensions_IExtensions_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Extensions_IExtensions_UninstallExtensionHandler"></a> UninstallExtensionHandler

Gets or sets a handler that is used when the extension is about to uninstall.

```csharp
IHandler<UninstallExtensionParameters, UninstallExtensionResponse> UninstallExtensionHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[UninstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionParameters), [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse)\>

##### Remarks

<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Uninstall" data-throw-if-not-resolved="false"></xref> value to uninstall the extension.</p>
<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> value to cancel the uninstalling.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Extensions_IExtensions_Install_System_String_"></a> Install\(string\)

Installs an extension from the local CRX file by the given <code class="paramref">path</code>.

```csharp
Task<IExtension> Install(string path)
```

##### Parameters

`path` [string](https://learn.microsoft.com/dotnet/api/system.string)

The path to the extension CRX3 package.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)\>

A task that completes when the extension installation is completed. If the installation is successful, the
result will contain an <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> instance that corresponds to the installed extension. If the
extension installation fails, the task will complete with an <xref href="DotNetBrowser.Extensions.ExtensionInstallationException" data-throw-if-not-resolved="false"></xref>
describing the error.

##### Remarks

<p>
    Extensions can be installed for an incognito profile.
</p>
<p>
    Extensions installed for the default profile in the engine with <xref href="DotNetBrowser.Engine.EngineOptions.IsIncognitoEnabled" data-throw-if-not-resolved="false"></xref>
    option set to <code>true</code> are also installed for the default profile. Extensions installed for the
    default profile in the engine with <xref href="DotNetBrowser.Engine.EngineOptions.IsIncognitoEnabled" data-throw-if-not-resolved="false"></xref> option set to <code>false</code>
    are not enabled when the engine is launched with this option.
</p>
<p>
    If the same extension is already installed, this method returns the already installed
    extension. If the extension version is newer than that is already installed,
    this method replaces the installed extension.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionInstalled"></a> ExtensionInstalled

Occurs when an extension is installed.

```csharp
event EventHandler<ExtensionInstalledEventArgs> ExtensionInstalled
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionInstalledEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionUninstalled"></a> ExtensionUninstalled

Occurs when an extension is uninstalled.

```csharp
event EventHandler<ExtensionUninstalledEventArgs> ExtensionUninstalled
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionUninstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionUpdated"></a> ExtensionUpdated

Occurs when an extension is updated.

```csharp
event EventHandler<ExtensionUpdatedEventArgs> ExtensionUpdated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUpdatedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Extensions_ExtensionActionType"></a> Enum ExtensionActionType

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

The extension action type.

```csharp
public enum ExtensionActionType
```

### Fields

`Action = 3` 

The chrome.action type available in Manifest V3.



`Browser = 2` 

The browser action can be applied to all web pages within a browser.



`Page = 1` 

The page action can be applied to some web pages, but is not applicable to all pages.

## <a id="DotNetBrowser_Extensions_ExtensionPermission"></a> Enum ExtensionPermission

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

The extension permission types.

```csharp
public enum ExtensionPermission
```

### Fields

`ActiveTab = 2` 

Gives temporary access to the active tab through a user gesture.



`Alarms = 3` 

Gives access to the chrome.alarms API.



`Background = 4` 

Makes Chrome start up early (as soon as the user logs into their computer—before the user
launches Chrome), and shut down late (even after its last window is closed until the user
explicitly quits Chrome).
In DotNetBrowser this permission has no effect.



`Bookmarks = 5` 

Gives access to the `chrome.bookmarks` API.



`BrowsingData = 6` 

Gives access to the `chrome.browsingData` API.



`CertificateProvider = 7` 

ChromeOS only. Gives access to the `chrome.certificateProvider` API.



`ClipboardRead = 8` 

Required if the extension uses `document.execCommand('paste')`.



`ClipboardWrite = 9` 

Required if the extension uses `document.execCommand('copy')` or `document.execCommand('cut')`.



`ContentSettings = 10` 

Gives access to the `chrome.contentSettings` API.



`ContextMenus = 11` 

Gives access to the `chrome.contextMenus` API.



`Cookies = 12` 

Gives access to the `chrome.cookies` API.



`Debugger = 13` 

Gives access to the `chrome.debugger` API.



`DeclarativeContent = 14` 

Gives access to the `chrome.declarativeContent` API.



`DeclarativeNetRequest = 15` 

Gives access to the `chrome.declarativeNetRequest` API.



`DeclarativeNetRequestFeedback = 17` 

Gives access to the `chrome.declarativeNetRequestFeedback` API which returns information on declarative rules
matched.



`DeclarativeNetRequestWithHostAccess = 16` 

Gives access to the `chrome.declarativeNetRequest` API, but requires host permissions to the request URL and
initiator to act on a request.



`DeclarativeWebRequest = 18` 

Gives access to the `chrome.declarativeWebRequest` API.
This API is deprecated. Check out the `chrome.declarativeNetRequest` API instead.



`DesktopCapture = 19` 

Gives access to the `chrome.desktopCapture` API.



`DocumentScan = 20` 

Gives access to the `chrome.documentScan` API.



`Downloads = 21` 

Gives access to the `chrome.downloads` API.

In DotNetBrowser the downloads API is not supported. Extensions are not allowed
to initiate downloads.

`DownloadsOpen = 69` 

The permission required to use the `chrome.downloads.open()` method.



`DownloadsUI = 70` 

The permission required to use the `chrome.downloads.setUiOptions()` method.In DotNetBrowser this method has no
effect.



`EnterpriseDeviceAttributes = 22` 

Gives access to the `chrome.enterprise.deviceAttributes` API.



`EnterpriseHardwarePlatform = 23` 

Gives access to the `chrome.enterprise.hardwarePlatform` API.



`EnterpriseNetworkingAttributes = 24` 

Gives access to the `chrome.enterprise.networkingAttributes` API.



`EnterprisePlatformKeys = 25` 

Gives access to the `chrome.enterprise.platformKeys` API.



`Experimental = 26` 

Gives access to the `chrome.experimental.*` APIs.



`FileBrowserHandler = 27` 

ChromeOS only. Gives access to the `chrome.fileBrowserHandler` API.



`FileSystemProvider = 28` 

ChromeOS only. Gives access to the `chrome.fileSystemProvider` API.



`FontSettings = 29` 

Gives access to the `chrome.fontSettings` API.



`Gcm = 30` 

Gives access to the `chrome.gcm` API.



`Geolocation = 31` 

Allows the extension to use the geolocation API without prompting the user for permission.



`History = 32` 

Gives access to the `chrome.history` API.



`Identity = 33` 

Gives access to the `chrome.identity` API.



`Idle = 34` 

Gives access to the `chrome.idle` API.



`LoginState = 35` 

ChromeOS only. Gives access to the `chrome.loginState` API.



`Management = 36` 

Gives access to the `chrome.management` API.



`NativeMessaging = 37` 

Gives access to the native messaging API.



`Notifications = 38` 

Gives access to the `chrome.notifications` API.



`Offscreen = 39` 

Gives access to the `chrome.offscreen` API.



`PageCapture = 40` 

Gives access to the `chrome.pageCapture` API.



`PlatformKeys = 41` 

ChromeOS only. Gives access to the `chrome.platformKeys` API.



`Power = 42` 

Gives access to the `chrome.power` API.



`PrinterProvider = 43` 

Gives access to the `chrome.printerProvider` API.



`Printing = 44` 

ChromeOS only. Gives access to the `chrome.printing` API.



`PrintingMetrics = 45` 

ChromeOS only. Gives access to the `chrome.printingMetrics` API.



`Privacy = 46` 

Gives access to the `chrome.privacy` API.



`Process = 47` 

Gives access to the `chrome.processes` API.



`Proxy = 48` 

Gives access to the `chrome.proxy` API.



`Scripting = 49` 

Gives access to the `chrome.scripting` API.



`Search = 50` 

Gives access to the `chrome.search` API.



`Sessions = 51` 

Gives access to the `chrome.sessions` API.



`Storage = 52` 

Gives access to the `chrome.storage` API.



`SystemCpu = 53` 

Gives access to the `chrome.system.cpu` API.



`SystemDisplay = 54` 

Gives access to the `chrome.system.display` API.



`SystemMemory = 55` 

Gives access to the `chrome.system.memory` API.



`SystemStorage = 56` 

Gives access to the `chrome.system.storage` API.



`TabCapture = 57` 

Gives access to the `chrome.tabCapture` API.



`TabGroups = 58` 

Gives access to the `chrome.tabGroups` API.



`Tabs = 59` 

Gives access to privileged fields of the Tab objects used by several APIs including `chrome.tabs` and
`chrome.windows`. In many circumstances your extension will not need
to declare the "tabs" permission to make use of these APIs.



`TopSites = 60` 

Gives access to the `chrome.topSites` API.



`Tts = 61` 

Gives access to the `chrome.tts` API.



`TtsEngine = 62` 

Gives access to the `chrome.ttsEngine` API.



`Unknown = 1` 

An unknown permission type.



`UnlimitedStorage = 63` 

Provides an unlimited quota for storing client-side data, such as databases and local storage files. Without this
permission, the extension is limited to 10 MB of local storage.

Note: This permission applies only to Web SQL Database and application cache (see issue 58985).
Also, it doesn't currently work with wildcard subdomains such as http://*.example.com.

`VpnProvider = 64` 

ChromeOS only. Gives access to the `chrome.vpnProvider` API.



`Wallpaper = 65` 

ChromeOS only. Gives access to the `chrome.wallpaper` API.



`WebAuthenticationProxy = 71` 

Gives access to the `chrome.webAuthenticationProxy` API.



`WebNavigation = 66` 

Gives access to the `chrome.webNavigation` API.



`WebRequest = 67` 

Gives access to the `chrome.webRequest` API.



`WebRequestBlocking = 68` 

Required if the extension uses the `chrome.webRequest` API in a blocking fashion.
