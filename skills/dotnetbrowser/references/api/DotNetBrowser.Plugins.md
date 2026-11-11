# <a id="DotNetBrowser_Plugins"></a> Namespace DotNetBrowser.Plugins

### Namespaces

 [DotNetBrowser.Plugins.Handlers](DotNetBrowser.Plugins.Handlers.md)

### Classes

 [Plugin](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_Plugin)

The detailed information about the installed Chromium plugin.

### Interfaces

 [IPluginSettings](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_IPluginSettings)

The settings to configure the available Chromium <xref href="DotNetBrowser.Plugins" data-throw-if-not-resolved="false"></xref>.

 [IPlugins](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_IPlugins)

The engine service that provides the details about the available Chromium plugins.

### Enums

 [PluginType](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_PluginType)

The plugin types.

## <a id="DotNetBrowser_Plugins_Plugin"></a> Class Plugin

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The detailed information about the installed Chromium plugin.

```csharp
public class Plugin
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Plugin](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_Plugin)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Plugins_Plugin_Description"></a> Description

Gets the plugin description.

```csharp
public string Description { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Plugins_Plugin_MimeTypes"></a> MimeTypes

Gets the MIME types supported by this plugin.

```csharp
public IEnumerable<MimeType> MimeTypes { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)\>

#### <a id="DotNetBrowser_Plugins_Plugin_Name"></a> Name

Gets the name of the plugin.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Plugins_Plugin_Path"></a> Path

Gets the plugin path representation.

```csharp
public string Path { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Plugins_Plugin_PluginType"></a> PluginType

Gets the plugin type.

```csharp
public PluginType PluginType { get; }
```

##### Property Value

 [PluginType](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_PluginType)

#### <a id="DotNetBrowser_Plugins_Plugin_Version"></a> Version

Gets the version number of the plugin file.

```csharp
public string Version { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Plugins_IPluginSettings"></a> Interface IPluginSettings

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The settings to configure the available Chromium <xref href="DotNetBrowser.Plugins" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IPluginSettings : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Plugins_IPluginSettings_PdfViewerEnabled"></a> PdfViewerEnabled

Enables or disables the built-in PDF viewer.

```csharp
bool PdfViewerEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPluginSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Plugins_IPlugins"></a> Interface IPlugins

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The engine service that provides the details about the available Chromium plugins.

```csharp
public interface IPlugins : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Plugins_IPlugins_AllowPluginHandler"></a> AllowPluginHandler

Gets or sets a handler that is used when the engine wants to check whether a specific plugin is allowed or
not.

```csharp
IHandler<AllowPluginParameters, AllowPluginResponse> AllowPluginHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[AllowPluginParameters](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginParameters), [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginResponse)\>

##### Remarks

<p>Use the <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse.Allow" data-throw-if-not-resolved="false"></xref> method to allow the plugin.</p>
<p>Use the <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse.Deny" data-throw-if-not-resolved="false"></xref> method to deny the plugin.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse.Allow" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    <b>Important:</b> the engine will be blocked until the callback response is sent. It is not
    allowed to invoke any engine/browser methods in this callback.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPlugins" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Plugins_IPlugins_AvailablePlugins"></a> AvailablePlugins

Gets the collection of the installed and available Chromium plugins.

```csharp
IEnumerable<Plugin> AvailablePlugins { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Plugin](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_Plugin)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPlugins" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Plugins_IPlugins_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Plugins_IPlugins_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Plugins_IPlugins_Settings"></a> Settings

Gets the settings of the available Chromium plugins.

```csharp
IPluginSettings Settings { get; }
```

##### Property Value

 [IPluginSettings](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_IPluginSettings)

## <a id="DotNetBrowser_Plugins_PluginType"></a> Enum PluginType

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The plugin types.

```csharp
public enum PluginType
```

### Fields

`BrowserInternalPlugin = 2` 

A browser internal plugin.



`BrowserPlugin = 1` 

A browser plugin.
