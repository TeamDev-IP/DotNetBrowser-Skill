# <a id="DotNetBrowser_Extensions_Handlers"></a> Namespace DotNetBrowser.Extensions.Handlers

### Classes

 [InstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionParameters)

The parameters of the <xref href="DotNetBrowser.Extensions.IExtensions.InstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

 [InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionResponse)

The response to the <xref href="DotNetBrowser.Extensions.IExtensions.InstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

 [OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters)

The parameters of the <xref href="DotNetBrowser.Extensions.IExtension.OpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

 [UninstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionParameters)

The parameters of the <xref href="DotNetBrowser.Extensions.IExtensions.UninstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

 [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse)

The response to the <xref href="DotNetBrowser.Extensions.IExtensions.UninstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters"></a> Class InstallExtensionParameters

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Extensions.IExtensions.InstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class InstallExtensionParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionCrxFile"></a> ExtensionCrxFile

Gets the absolute path to the CRX file the extension is about to be installed from.

```csharp
public string ExtensionCrxFile { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    The file will be automatically deleted after the installation is completed or
    canceled. You can make a copy of the CRX file and store it for future use.
    For example, you can use the file to pack the extension into the application bundle and
    install it programmatically using
    <xref href="DotNetBrowser.Extensions.IExtensions.Install(System.String)" data-throw-if-not-resolved="false"></xref>
</p>

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionId"></a> ExtensionId

Gets the ID of the extension to install.

```csharp
public string ExtensionId { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionName"></a> ExtensionName

Gets the name of the extension to install.

```csharp
public string ExtensionName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionVersion"></a> ExtensionVersion

Gets the version of the extension to install.

```csharp
public string ExtensionVersion { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_Hosts"></a> Hosts

Gets the hosts that the extension requests access to.

```csharp
public IReadOnlyList<string> Hosts { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Remarks

<p>
    The values are represented in the form of
    <a href="https://developer.chrome.com/docs/extensions/mv3/match_patterns/">
        matches pattern
    </a>
    .
</p>
<p>
    Please note that values are being processed by engine and might be not equal to
    the extension manifest values. For example, some slashes and wildcards could be added.
</p>

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_Permissions"></a> Permissions

Gets the required extension permissions.

```csharp
public IReadOnlyList<ExtensionPermission> Permissions { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ExtensionPermission](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_ExtensionPermission)\>

## <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionResponse"></a> Class InstallExtensionResponse

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Extensions.IExtensions.InstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class InstallExtensionResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionResponse_Cancel"></a> Cancel

The <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension installation should be
canceled.

```csharp
public static InstallExtensionResponse Cancel
```

##### Field Value

 [InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionResponse)

#### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionResponse_Install"></a> Install

The <xref href="DotNetBrowser.Extensions.Handlers.InstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension should be
installed.

```csharp
public static InstallExtensionResponse Install
```

##### Field Value

 [InstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_InstallExtensionResponse)

## <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters"></a> Class OpenExtensionPopupParameters

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Extensions.IExtension.OpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExtensionPopupParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_Extension"></a> Extension

Gets the extension that requests opening the popup.

```csharp
public IExtension Extension { get; }
```

##### Property Value

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

#### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the created popup browser.

```csharp
public IBrowser PopupBrowser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_Url"></a> Url

Gets the URL of the popup.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionParameters"></a> Class UninstallExtensionParameters

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Extensions.IExtensions.UninstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UninstallExtensionParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UninstallExtensionParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionParameters_Extension"></a> Extension

Gets the extension that is about to be uninstalled.

```csharp
public IExtension Extension { get; }
```

##### Property Value

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

## <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse"></a> Class UninstallExtensionResponse

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Extensions.IExtensions.UninstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UninstallExtensionResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse_Cancel"></a> Cancel

The <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension uninstalling should be
canceled.

```csharp
public static UninstallExtensionResponse Cancel
```

##### Field Value

 [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse)

#### <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse_Uninstall"></a> Uninstall

The <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension should be
uninstalled.

```csharp
public static UninstallExtensionResponse Uninstall
```

##### Field Value

 [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse)
