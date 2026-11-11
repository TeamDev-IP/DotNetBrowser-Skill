# <a id="DotNetBrowser_Permissions_Handlers"></a> Namespace DotNetBrowser.Permissions.Handlers

### Classes

 [RequestPermissionParameters](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionParameters)

The parameters of the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

 [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionResponse)

A response to the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters"></a> Class RequestPermissionParameters

Namespace: [DotNetBrowser.Permissions.Handlers](DotNetBrowser.Permissions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPermissionParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPermissionParameters](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters_Type"></a> Type

Gets the permission type of the current request.

```csharp
public PermissionType Type { get; }
```

##### Property Value

 [PermissionType](DotNetBrowser.Permissions.md#DotNetBrowser_Permissions_PermissionType)

#### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters_Url"></a> Url

Gets the URL of the web page that requests permission.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse"></a> Class RequestPermissionResponse

Namespace: [DotNetBrowser.Permissions.Handlers](DotNetBrowser.Permissions.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPermissionResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that permission is denied.

```csharp
public static RequestPermissionResponse Deny()
```

##### Returns

 [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionResponse)

The <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionResponse_Grant"></a> Grant\(\)

Creates a <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that permission is granted.

```csharp
public static RequestPermissionResponse Grant()
```

##### Returns

 [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.md#DotNetBrowser_Permissions_Handlers_RequestPermissionResponse)

The <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref> implementation.
