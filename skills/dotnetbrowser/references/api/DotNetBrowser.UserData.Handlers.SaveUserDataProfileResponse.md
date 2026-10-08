# <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse"></a> Class SaveUserDataProfileResponse

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveUserDataProfileResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse_Decline"></a> Decline

Creates a <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to decline
to save the user data profile.

```csharp
public static SaveUserDataProfileResponse Decline
```

#### Field Value

 [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md)

### <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse_Save"></a> Save

Creates a <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to save
the user data profile to the <xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+store" data-throw-if-not-resolved="false"></xref>.

```csharp
public static SaveUserDataProfileResponse Save
```

#### Field Value

 [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md)

