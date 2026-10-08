# <a id="DotNetBrowser_Plugins_IPlugins"></a> Interface IPlugins

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The engine service that provides the details about the available Chromium plugins.

```csharp
public interface IPlugins : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Plugins_IPlugins_AllowPluginHandler"></a> AllowPluginHandler

Gets or sets a handler that is used when the engine wants to check whether a specific plugin is allowed or
not.

```csharp
IHandler<AllowPluginParameters, AllowPluginResponse> AllowPluginHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[AllowPluginParameters](DotNetBrowser.Plugins.Handlers.AllowPluginParameters.md), [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.AllowPluginResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPlugins" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Plugins_IPlugins_AvailablePlugins"></a> AvailablePlugins

Gets the collection of the installed and available Chromium plugins.

```csharp
IEnumerable<Plugin> AvailablePlugins { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Plugin](DotNetBrowser.Plugins.Plugin.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Plugins.IPlugins" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Plugins_IPlugins_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Plugins_IPlugins_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Plugins_IPlugins_Settings"></a> Settings

Gets the settings of the available Chromium plugins.

```csharp
IPluginSettings Settings { get; }
```

#### Property Value

 [IPluginSettings](DotNetBrowser.Plugins.IPluginSettings.md)

