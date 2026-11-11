# <a id="DotNetBrowser_UserData_Handlers"></a> Namespace DotNetBrowser.UserData.Handlers

### Classes

 [SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters)

The parameters of the <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

 [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse)

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

 [UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters)

The parameters of the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

 [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse)

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters"></a> Class SaveUserDataProfileParameters

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveUserDataProfileParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters_UserDataProfile"></a> UserDataProfile

Gets the user data profile entered in a web form.

```csharp
public UserDataProfile UserDataProfile { get; }
```

##### Property Value

 [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

## <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse"></a> Class SaveUserDataProfileResponse

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveUserDataProfileResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse_Decline"></a> Decline

Creates a <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to decline
to save the user data profile.

```csharp
public static SaveUserDataProfileResponse Decline
```

##### Field Value

 [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse)

#### <a id="DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse_Save"></a> Save

Creates a <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to save
the user data profile to the <xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+store" data-throw-if-not-resolved="false"></xref>.

```csharp
public static SaveUserDataProfileResponse Save
```

##### Field Value

 [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse)

## <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters"></a> Class UpdateUserDataProfileParameters

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdateUserDataProfileParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters_OriginalUserDataProfile"></a> OriginalUserDataProfile

Gets the original user data profile that is about to be updated.

```csharp
public UserDataProfile OriginalUserDataProfile { get; }
```

##### Property Value

 [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

#### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters_UserDataProfile"></a> UserDataProfile

Gets the new user data profile that is about to replace the <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.OriginalUserDataProfile?text=original+profile" data-throw-if-not-resolved="false"></xref>.

```csharp
public UserDataProfile UserDataProfile { get; }
```

##### Property Value

 [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

## <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse"></a> Class UpdateUserDataProfileResponse

Namespace: [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.UserData.IUserDataProfiles.UpdateUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdateUserDataProfileResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse_Decline"></a> Decline

Creates a <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to decline
to update the user data profile.

```csharp
public static UpdateUserDataProfileResponse Decline
```

##### Field Value

 [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse)

#### <a id="DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse_Update"></a> Update

Creates a <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to update
the user data profile in the <xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+store" data-throw-if-not-resolved="false"></xref>.

```csharp
public static UpdateUserDataProfileResponse Update
```

##### Field Value

 [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse)
