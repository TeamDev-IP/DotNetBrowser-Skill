# <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse"></a> Class AllowPluginResponse

Namespace: [DotNetBrowser.Plugins.Handlers](DotNetBrowser.Plugins.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AllowPluginResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AllowPluginResponse](DotNetBrowser.Plugins.Handlers.AllowPluginResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse_Allow"></a> Allow\(\)

Creates an <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the plugin is allowed to be used.

```csharp
public static AllowPluginResponse Allow()
```

#### Returns

 [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.AllowPluginResponse.md)

The <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse_Deny"></a> Deny\(\)

Creates an <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the plugin isn't allowed at the moment.

```csharp
public static AllowPluginResponse Deny()
```

#### Returns

 [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.AllowPluginResponse.md)

The <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref> implementation.

