
# Permissions

**Lead**
This guide shows how to grant or deny permissions for websites.


It is possible to handle the case when a web page requests a permission, for example, to enable geolocation. These permissions can be granted or denied by setting up a permission handler. See the code sample below:


**C#**
```csharp
// Grant all permissions.
engine.Profiles.Default.Permissions.RequestPermissionHandler =
    new Handler<RequestPermissionParameters, RequestPermissionResponse>(p =>
    {
        return RequestPermissionResponse.Grant();
    });
```

**VB**
```vb
' Grant all permissions.
engine.Profiles.Default.Permissions.RequestPermissionHandler = 
    New Handler(Of RequestPermissionParameters, RequestPermissionResponse)(Function(p)
        Return RequestPermissionResponse.Grant()
    End Function)
```



You can also grant a specific permission only:


**C#**
```csharp
// Grant Geolocation permission.
engine.Profiles.Default.Permissions.RequestPermissionHandler =
    new Handler<RequestPermissionParameters, RequestPermissionResponse>(p =>
    {
        if(p.Type == PermissionType.Geolocation)
        {
            return RequestPermissionResponse.Grant();
        }
        return RequestPermissionResponse.Deny();
    });
```

**VB**
```vb
' Grant Geolocation permission.
engine.Profiles.Default.Permissions.RequestPermissionHandler = 
    New Handler(Of RequestPermissionParameters, RequestPermissionResponse)(Function(p)
        If p.Type = PermissionType.Geolocation Then
            Return RequestPermissionResponse.Grant()
        End If
        Return RequestPermissionResponse.Deny()
    End Function)
```


