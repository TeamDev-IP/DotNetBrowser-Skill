# <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters"></a> Class RequestPermissionParameters

Namespace: [DotNetBrowser.Permissions.Handlers](DotNetBrowser.Permissions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Permissions.IPermissions.RequestPermissionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPermissionParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPermissionParameters](DotNetBrowser.Permissions.Handlers.RequestPermissionParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters_Type"></a> Type

Gets the permission type of the current request.

```csharp
public PermissionType Type { get; }
```

#### Property Value

 [PermissionType](DotNetBrowser.Permissions.PermissionType.md)

### <a id="DotNetBrowser_Permissions_Handlers_RequestPermissionParameters_Url"></a> Url

Gets the URL of the web page that requests permission.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

