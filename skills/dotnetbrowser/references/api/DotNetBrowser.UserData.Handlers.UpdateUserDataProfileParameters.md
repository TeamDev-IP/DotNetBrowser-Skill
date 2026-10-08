# <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters"></a> Class UpdateUserDataProfileParameters

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdateUserDataProfileParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters_OriginalUserDataProfile"></a> OriginalUserDataProfile

Gets the original user data profile that is about to be updated.

```csharp
public UserDataProfile OriginalUserDataProfile { get; }
```

#### Property Value

 [UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)

### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters_UserDataProfile"></a> UserDataProfile

Gets the new user data profile that is about to replace the <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.OriginalUserDataProfile?text=original+profile" data-throw-if-not-resolved="false"></xref>.

```csharp
public UserDataProfile UserDataProfile { get; }
```

#### Property Value

 [UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)

