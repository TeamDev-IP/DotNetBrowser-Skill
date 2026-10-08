# <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse"></a> Class RequestPermissionResponse

Namespace: [DotNetBrowser.Permissions.Handlers](DotNetBrowser.Permissions.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPermissionResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that permission is denied.

```csharp
public static RequestPermissionResponse Deny()
```

#### Returns

 [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.md)

The <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse_Grant"></a> Grant\(\)

Creates a <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that permission is granted.

```csharp
public static RequestPermissionResponse Grant()
```

#### Returns

 [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.md)

The <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref> implementation.

