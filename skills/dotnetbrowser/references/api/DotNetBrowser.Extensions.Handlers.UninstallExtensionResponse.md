# <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse"></a> Class UninstallExtensionResponse

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Extensions.IExtensions.UninstallExtensionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UninstallExtensionResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse_Cancel"></a> Cancel

The <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension uninstalling should be
canceled.

```csharp
public static UninstallExtensionResponse Cancel
```

#### Field Value

 [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.md)

### <a id="DotNetBrowser_Extensions_Handlers_UninstallExtensionResponse_Uninstall"></a> Uninstall

The <xref href="DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the extension should be
uninstalled.

```csharp
public static UninstallExtensionResponse Uninstall
```

#### Field Value

 [UninstallExtensionResponse](DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.md)

