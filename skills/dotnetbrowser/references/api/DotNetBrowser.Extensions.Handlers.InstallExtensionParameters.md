# <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters"></a> Class InstallExtensionParameters

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Extensions.IExtensions.InstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class InstallExtensionParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InstallExtensionParameters](DotNetBrowser.Extensions.Handlers.InstallExtensionParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionCrxFile"></a> ExtensionCrxFile

Gets the absolute path to the CRX file the extension is about to be installed from.

```csharp
public string ExtensionCrxFile { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    The file will be automatically deleted after the installation is completed or
    canceled. You can make a copy of the CRX file and store it for future use.
    For example, you can use the file to pack the extension into the application bundle and
    install it programmatically using
    <xref href="DotNetBrowser.Extensions.IExtensions.Install(System.String)" data-throw-if-not-resolved="false"></xref>
</p>

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionId"></a> ExtensionId

Gets the ID of the extension to install.

```csharp
public string ExtensionId { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionName"></a> ExtensionName

Gets the name of the extension to install.

```csharp
public string ExtensionName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_ExtensionVersion"></a> ExtensionVersion

Gets the version of the extension to install.

```csharp
public string ExtensionVersion { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_Hosts"></a> Hosts

Gets the hosts that the extension requests access to.

```csharp
public IReadOnlyList<string> Hosts { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Remarks

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

### <a id="DotNetBrowser_Extensions_Handlers_InstallExtensionParameters_Permissions"></a> Permissions

Gets the required extension permissions.

```csharp
public IReadOnlyList<ExtensionPermission> Permissions { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ExtensionPermission](DotNetBrowser.Extensions.ExtensionPermission.md)\>

