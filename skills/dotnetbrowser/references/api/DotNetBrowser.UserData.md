# <a id="DotNetBrowser_UserData"></a> Namespace DotNetBrowser.UserData

### Namespaces

 [DotNetBrowser.UserData.Handlers](DotNetBrowser.UserData.Handlers.md)

### Classes

 [Address](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address)

The user's address containing information about a street, city, state, etc.

 [Address.Builder](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address_Builder)

A builder for the <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> class.

 [UserDataProfile.Builder](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile_Builder)

A builder for creating a new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance.

 [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

The collected data entered by the user to a form and persisted to
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=the+user+data+store" data-throw-if-not-resolved="false"></xref>.

### Interfaces

 [IUserDataProfileStore](DotNetBrowser.UserData.md#DotNetBrowser_UserData_IUserDataProfileStore)

The data store for <xref href="DotNetBrowser.UserData.UserDataProfile?text=the+user+data" data-throw-if-not-resolved="false"></xref>.

 [IUserDataProfiles](DotNetBrowser.UserData.md#DotNetBrowser_UserData_IUserDataProfiles)

A service that allows managing user data profiles.

## <a id="DotNetBrowser_UserData_Address"></a> Class Address

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

The user's address containing information about a street, city, state, etc.

```csharp
public sealed class Address
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Address](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_Address_City"></a> City

Gets the city from the address.

```csharp
public string City { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_CountryCode"></a> CountryCode

Gets the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO 3166</a>
2-letter country code.

```csharp
public string CountryCode { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_DependentLocality"></a> DependentLocality

Gets the subdivision of a city, e.g. inner-city district or suburb.

```csharp
public string DependentLocality { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_State"></a> State

Gets the name of the state.

```csharp
public string State { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Street"></a> Street

Gets the whole street name.

```csharp
public string Street { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Zip"></a> Zip

Gets the ZIP code entered by the user.

```csharp
public string Zip { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_UserData_Address_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_UserData_Address_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_UserData_Address_Builder"></a> Class Address.Builder

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A builder for the <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> class.

```csharp
public sealed class Address.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Address.Builder](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_Address_Builder_City"></a> City

Gets or sets the city from the address.

```csharp
public string City { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Builder_CountryCode"></a> CountryCode

Gets or sets the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO 3166</a>
country code.

```csharp
public string CountryCode { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Builder_DependentLocality"></a> DependentLocality

Gets or sets the subdivision of a city, e.g. inner-city district or suburb.

```csharp
public string DependentLocality { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Builder_State"></a> State

Gets or sets the name of the state.

```csharp
public string State { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Builder_Street"></a> Street

Gets or sets the whole street name.

```csharp
public string Street { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_Address_Builder_Zip"></a> Zip

Gets or sets the ZIP code entered by the user.

```csharp
public string Zip { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_UserData_Address_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Address Build()
```

##### Returns

 [Address](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address)

A new <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_UserData_UserDataProfile"></a> Class UserDataProfile

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

The collected data entered by the user to a form and persisted to
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=the+user+data+store" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UserDataProfile
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_UserDataProfile_Address"></a> Address

Gets the address entered by the user.

```csharp
public Address Address { get; }
```

##### Property Value

 [Address](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address)

#### <a id="DotNetBrowser_UserData_UserDataProfile_CompanyName"></a> CompanyName

Gets the name of the company entered by the user.

```csharp
public string CompanyName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_Email"></a> Email

Gets the email value entered by the user.

```csharp
public string Email { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_FullName"></a> FullName

Gets the full name value entered by the user.

```csharp
public string FullName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_PhoneNumber"></a> PhoneNumber

Gets the phone number value entered by the user.

```csharp
public string PhoneNumber { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_UserData_UserDataProfile_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_UserData_UserDataProfile_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_UserData_UserDataProfile_Builder"></a> Class UserDataProfile.Builder

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class UserDataProfile.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserDataProfile.Builder](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Address"></a> Address

Gets or sets the address entered by the user.

```csharp
public Address Address { get; set; }
```

##### Property Value

 [Address](DotNetBrowser.UserData.md#DotNetBrowser_UserData_Address)

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_CompanyName"></a> CompanyName

Gets or sets the name of the company entered by the user.

```csharp
public string CompanyName { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Email"></a> Email

Gets or sets the email entered by the user.

```csharp
public string Email { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_FullName"></a> FullName

Gets or sets the full name entered by the user.

```csharp
public string FullName { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_PhoneNumber"></a> PhoneNumber

Gets or sets the phone number entered by the user.

```csharp
public string PhoneNumber { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance with the properties set in the builder.

```csharp
public UserDataProfile Build()
```

##### Returns

 [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

A new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_UserData_IUserDataProfileStore"></a> Interface IUserDataProfileStore

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

The data store for <xref href="DotNetBrowser.UserData.UserDataProfile?text=the+user+data" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IUserDataProfileStore
```

### Properties

#### <a id="DotNetBrowser_UserData_IUserDataProfileStore_All"></a> All

Gets all user data records.

```csharp
IReadOnlyList<UserDataProfile> All { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)\>

##### Remarks

The user data records are saved to the store via <xref href="DotNetBrowser.UserData.IUserDataProfiles.SaveUserDataProfileHandler" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

### Methods

#### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Add_DotNetBrowser_UserData_UserDataProfile_"></a> Add\(UserDataProfile\)

Adds the user data to the store.

```csharp
void Add(UserDataProfile userDataProfile)
```

##### Parameters

`userDataProfile` [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

The user data to add.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The user data is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The user data validation has failed.

#### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Clear"></a> Clear\(\)

Clears all records in the store.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_UserData_IUserDataProfileStore_Remove_DotNetBrowser_UserData_UserDataProfile_"></a> Remove\(UserDataProfile\)

Removes the user data from the store.

```csharp
void Remove(UserDataProfile userDataProfile)
```

##### Parameters

`userDataProfile` [UserDataProfile](DotNetBrowser.UserData.md#DotNetBrowser_UserData_UserDataProfile)

The user data profile associated with the removed user data profile records.

##### Remarks

Removed user data is not displayed in the autofill suggestion pop-up.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfileStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">userDataProfile</code> is null.

## <a id="DotNetBrowser_UserData_IUserDataProfiles"></a> Interface IUserDataProfiles

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing user data profiles.

```csharp
public interface IUserDataProfiles : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_UserData_IUserDataProfiles_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_UserData_IUserDataProfiles_SaveUserDataProfileHandler"></a> SaveUserDataProfileHandler

Gets or sets a handler that is used when the user is prompted to save the user data profile to the
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=%0a++++++++++++user+data+profile+store%0a++++++++" data-throw-if-not-resolved="false"></xref>
.

```csharp
IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse> SaveUserDataProfileHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters), [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileResponse)\>

##### Remarks

<p>
    This handler is equivalent to the "Save Address?" bubble in Chromium.
</p>
<p>
    The handler is invoked when the user submits a web form where fields are associated with a
    user data profile such as city, state, street, zip code, email address, etc.
</p>
<p>
    Use the <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.Save" data-throw-if-not-resolved="false"></xref> to save this user data profile to the autofill
    store. All saved user data profiles are shown in the suggestion pop-up when focusing the web
    form control.
</p>
<p>
    Use the <xref href="DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.Decline" data-throw-if-not-resolved="false"></xref> to decline to save the user data profile. If the
    current profile is declined then the callback will be invoked again when submitting the web form
    with the same user data.
</p>
<p>
    The handler is not invoked if <xref href="DotNetBrowser.Profile.IProfilePreferences.AutofillEnabled?text=autofill" data-throw-if-not-resolved="false"></xref> is disabled.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_UserData_IUserDataProfiles_UpdateUserDataProfileHandler"></a> UpdateUserDataProfileHandler

Gets or sets a handler that is used when the user is prompted to update the user data profile to the
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+profile+store" data-throw-if-not-resolved="false"></xref>. For example, when the user changes the
<xref href="DotNetBrowser.UserData.UserDataProfile.Email?text=email+address" data-throw-if-not-resolved="false"></xref> to an empty string.

```csharp
IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse> UpdateUserDataProfileHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters), [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileResponse)\>

##### Remarks

<p>
    This callback is equivalent to the "Update Address?" bubble in Chromium.
</p>
<p>
    The handler is invoked when the user submits a web form where fields are associated with a
    user data profile such as city, state, street, zip code, email address, etc.
</p>
<p>
    Use the <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.Update" data-throw-if-not-resolved="false"></xref> to update the user data profile in the autofill
    data store.
</p>
<p>
    Use the <xref href="DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.Decline" data-throw-if-not-resolved="false"></xref> to decline to update the user data profile. If
    the current user data profile is declined then the callback will be invoked again when
    submitting the web form with the same user data.
</p>
<p>
    The handler is not invoked if <xref href="DotNetBrowser.Profile.IProfilePreferences.AutofillEnabled?text=autofill" data-throw-if-not-resolved="false"></xref> is disabled.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> has already been disposed.
