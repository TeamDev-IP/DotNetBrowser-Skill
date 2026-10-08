# <a id="DotNetBrowser_UserData_IUserDataProfiles"></a> Interface IUserDataProfiles

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing user data profiles.

```csharp
public interface IUserDataProfiles : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_UserData_IUserDataProfiles_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_UserData_IUserDataProfiles_SaveUserDataProfileHandler"></a> SaveUserDataProfileHandler

Gets or sets a handler that is used when the user is prompted to save the user data profile to the
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=%0a++++++++++++user+data+profile+store%0a++++++++" data-throw-if-not-resolved="false"></xref>
.

```csharp
IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse> SaveUserDataProfileHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.SaveUserDataProfileParameters.md), [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_UserData_IUserDataProfiles_UpdateUserDataProfileHandler"></a> UpdateUserDataProfileHandler

Gets or sets a handler that is used when the user is prompted to update the user data profile to the
<xref href="DotNetBrowser.UserData.IUserDataProfileStore?text=user+data+profile+store" data-throw-if-not-resolved="false"></xref>. For example, when the user changes the
<xref href="DotNetBrowser.UserData.UserDataProfile.Email?text=email+address" data-throw-if-not-resolved="false"></xref> to an empty string.

```csharp
IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse> UpdateUserDataProfileHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.md), [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> has already been disposed.

