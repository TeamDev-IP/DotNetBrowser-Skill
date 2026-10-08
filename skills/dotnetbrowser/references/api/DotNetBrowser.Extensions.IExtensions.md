# <a id="DotNetBrowser_Extensions_IExtensions"></a> Interface IExtensions

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing extensions.

```csharp
public interface IExtensions : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Extensions_IExtensions_All"></a> All

Gets all extensions that are currently installed for the profile.

```csharp
IReadOnlyCollection<IExtension> All { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[IExtension](DotNetBrowser.Extensions.IExtension.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensions_InstallExtensionHandler"></a> InstallExtensionHandler

Gets or sets a handler that is used when the user installs an extension from Chrome Web Store.

```csharp
IHandler<InstallExtensionParameters, InstallExtensionResponse> InstallExtensionHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[InstallExtensionParameters](DotNetBrowser.Extensions.Handlers.InstallExtensionParameters.md), [InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.md)\>

#### Remarks

<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Install" data-throw-if-not-resolved="false"></xref> value to install the extension.</p>
<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> value to cancel the installation.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Extensions_IExtensions_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Extensions_IExtensions_UninstallExtensionHandler"></a> UninstallExtensionHandler

Gets or sets a handler that is used when the extension is about to uninstall.

```csharp
IHandler<UninstallExtensionParameters, UninstallExtensionResponse> UninstallExtensionHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[UninstallExtensionParameters](DotNetBrowser.Extensions.Handlers.UninstallExtensionParameters.md), [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.md)\>

#### Remarks

<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Uninstall" data-throw-if-not-resolved="false"></xref> value to uninstall the extension.</p>
<p>Use the <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> value to cancel the uninstalling.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Extensions_IExtensions_Install_System_String_"></a> Install\(string\)

Installs an extension from the local CRX file by the given <code class="paramref">path</code>.

```csharp
Task<IExtension> Install(string path)
```

#### Parameters

`path` [string](https://learn.microsoft.com/dotnet/api/system.string)

The path to the extension CRX3 package.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IExtension](DotNetBrowser.Extensions.IExtension.md)\>

A task that completes when the extension installation is completed. If the installation is successful, the
result will contain an <xref href="DotNetBrowser.Extensions.IExtension" data-throw-if-not-resolved="false"></xref> instance that corresponds to the installed extension. If the
extension installation fails, the task will complete with an <xref href="DotNetBrowser.Extensions.ExtensionInstallationException" data-throw-if-not-resolved="false"></xref>
describing the error.

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionInstalled"></a> ExtensionInstalled

Occurs when an extension is installed.

```csharp
event EventHandler<ExtensionInstalledEventArgs> ExtensionInstalled
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.ExtensionInstalledEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionUninstalled"></a> ExtensionUninstalled

Occurs when an extension is uninstalled.

```csharp
event EventHandler<ExtensionUninstalledEventArgs> ExtensionUninstalled
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionUninstalledEventArgs](DotNetBrowser.Extensions.Events.ExtensionUninstalledEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Extensions_IExtensions_ExtensionUpdated"></a> ExtensionUpdated

Occurs when an extension is updated.

```csharp
event EventHandler<ExtensionUpdatedEventArgs> ExtensionUpdated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.ExtensionUpdatedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensions" data-throw-if-not-resolved="false"></xref> has already been disposed.

