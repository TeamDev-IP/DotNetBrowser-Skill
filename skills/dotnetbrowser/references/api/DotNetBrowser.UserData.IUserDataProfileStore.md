# <a id="DotNetBrowser_UserData_IUserDataProfileStore"></a> Interface IUserDataProfileStore

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

The data store for <xref href="DotNetBrowser.UserData.UserDataProfile?text=the+user+data" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IUserDataProfileStore
```

## Properties

### <a id="DotNetBrowser_UserData_IUserDataProfileStore_All"></a> All

Gets all user data records.

```csharp
IReadOnlyList<UserDataProfile> All { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)\>

#### Remarks

The user data records are saved to the store via <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Add_DotNetBrowser_UserData_UserDataProfile_"></a> Add\(UserDataProfile\)

Adds the user data to the store.

```csharp
void Add(UserDataProfile userDataProfile)
```

#### Parameters

`userDataProfile` [UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)

The user data to add.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The user data is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The user data validation has failed.

### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Clear"></a> Clear\(\)

Clears all records in the store.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Remove_DotNetBrowser_UserData_UserDataProfile_"></a> Remove\(UserDataProfile\)

Removes the user data from the store.

```csharp
void Remove(UserDataProfile userDataProfile)
```

#### Parameters

`userDataProfile` [UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)

The user data profile associated with the removed user data profile records.

#### Remarks

Removed user data is not displayed in the autofill suggestion pop-up.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">userDataProfile</code> is null.

