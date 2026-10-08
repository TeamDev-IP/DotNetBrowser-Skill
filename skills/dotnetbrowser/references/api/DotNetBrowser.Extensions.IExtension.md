# <a id="DotNetBrowser_Extensions_IExtension"></a> Interface IExtension

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

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

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

## Properties

### <a id="DotNetBrowser_Extensions_IExtension_HasAction"></a> HasAction

Indicates whether an extension has an action.

```csharp
bool HasAction { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtension_Id"></a> Id

Gets the identifier of the extension.

```csharp
string Id { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtension_Name"></a> Name

Gets the name of the extension.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtension_OpenExtensionPopupHandler"></a> OpenExtensionPopupHandler

Gets or sets a handler that is used when the extension is about to open a popup window.

```csharp
IHandler<OpenExtensionPopupParameters> OpenExtensionPopupHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.OpenExtensionPopupParameters.md)\>

#### Remarks

The callback is invoked by the following extension API functions:

<ul><li><code>chrome.tabs.create</code>,</li><li><code>chrome.windows.create</code>,</li><li><code>chrome.runtime.openOptionsPage</code>,</li><li><code>setUninstallURL</code>, upon uninstalling an extension.</li></ul>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtension_Profile"></a> Profile

Gets the profile instance associated with this extension.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Extensions_IExtension_GetAction_DotNetBrowser_Browser_IBrowser_"></a> GetAction\(IBrowser\)

Gets the extension action for the given <code class="paramref">browser</code>.

```csharp
IExtensionAction GetAction(IBrowser browser)
```

#### Parameters

`browser` [IBrowser](DotNetBrowser.Browser.IBrowser.md)

The browser that will be associated with the action.

#### Returns

 [IExtensionAction](DotNetBrowser.Extensions.IExtensionAction.md)

The extension action for the passed browser or <code>null</code> if the action is not available.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtension_Uninstall"></a> Uninstall\(\)

Uninstalls this extension.

```csharp
Task<bool> Uninstall()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

A task that completes when the extension is uninstalled. The result value is <code>true</code> if the extension was
uninstalled successfully, <code>false</code> otherwise.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

