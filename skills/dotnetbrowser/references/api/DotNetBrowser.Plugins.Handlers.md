# <a id="DotNetBrowser_Plugins_Handlers"></a> Namespace DotNetBrowser.Plugins.Handlers

### Classes

 [AllowPluginParameters](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginParameters)

The parameters for the <xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref>.

 [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginResponse)

A response to the <xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Plugins_Handlers_AllowPluginParameters"></a> Class AllowPluginParameters

Namespace: [DotNetBrowser.Plugins.Handlers](DotNetBrowser.Plugins.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters for the <xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AllowPluginParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AllowPluginParameters](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Plugins_Handlers_AllowPluginParameters_Plugin"></a> Plugin

Gets the information about the plugin to check.

```csharp
public Plugin Plugin { get; }
```

##### Property Value

 [Plugin](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_Plugin)

## <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse"></a> Class AllowPluginResponse

Namespace: [DotNetBrowser.Plugins.Handlers](DotNetBrowser.Plugins.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AllowPluginResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AllowPluginResponse](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse_Allow"></a> Allow\(\)

Creates an <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the plugin is allowed to be used.

```csharp
public static AllowPluginResponse Allow()
```

##### Returns

 [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginResponse)

The <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Plugins_Handlers_AllowPluginResponse_Deny"></a> Deny\(\)

Creates an <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the plugin isn't allowed at the moment.

```csharp
public static AllowPluginResponse Deny()
```

##### Returns

 [AllowPluginResponse](DotNetBrowser.Plugins.Handlers.md#DotNetBrowser_Plugins_Handlers_AllowPluginResponse)

The <xref href="DotNetBrowser.Plugins.Handlers.AllowPluginResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Plugins.IPlugins.AllowPluginHandler" data-throw-if-not-resolved="false"></xref> implementation.
