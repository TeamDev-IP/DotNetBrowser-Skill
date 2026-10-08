# <a id="DotNetBrowser_Permissions_IPermissions"></a> Interface IPermissions

Namespace: [DotNetBrowser.Permissions](DotNetBrowser.Permissions.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing permissions.

```csharp
public interface IPermissions : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Permissions_IPermissions_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Permissions_IPermissions_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Permissions_IPermissions_RequestPermissionHandler"></a> RequestPermissionHandler

Gets or sets a handler that is used when a web page requests a permission, for example to enable geolocation.
The permission type and the information about the web page can be obtained from the passed request object.

```csharp
IHandler<RequestPermissionParameters, RequestPermissionResponse> RequestPermissionHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[RequestPermissionParameters](DotNetBrowser.Permissions.Handlers.RequestPermissionParameters.md), [RequestPermissionResponse](DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.Grant" data-throw-if-not-resolved="false"></xref> to grant the requested permission.
</p>
<p>
    Use the <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.Deny" data-throw-if-not-resolved="false"></xref> to deny the requested permission.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.Deny" data-throw-if-not-resolved="false"></xref>  will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Permissions.IPermissions" data-throw-if-not-resolved="false"></xref> has already been disposed.

