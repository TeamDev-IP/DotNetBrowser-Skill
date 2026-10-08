# <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse"></a> Class UpdateUserDataProfileResponse

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdateUserDataProfileResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse_Decline"></a> Decline

Creates a <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to decline
to update the user data profile.

```csharp
public static UpdateUserDataProfileResponse Decline
```

#### Field Value

 [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md)

### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse_Update"></a> Update

Creates a <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to update
the user data profile in the <xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+store" data-throw-if-not-resolved="false"></xref>.

```csharp
public static UpdateUserDataProfileResponse Update
```

#### Field Value

 [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md)

