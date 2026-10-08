# <a id="DotNetBrowser_Passwords_IPasswords"></a> Interface IPasswords

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing passwords.

```csharp
public interface IPasswords : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Passwords_IPasswords_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Passwords_IPasswords_SavePasswordHandler"></a> SavePasswordHandler

Gets or sets a handler that is used when the user is prompted to save the credentials in the
<xref href="DotNetBrowser.Passwords.IPasswordStore?text=%0a++++++++++++password+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<SavePasswordParameters, SavePasswordResponse> SavePasswordHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.SavePasswordParameters.md), [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)\>

#### Remarks

<p>
    This handler is equivalent to the "Save Password?" bubble in Chromium.
</p>
<p>
    The handler is invoked when the user submits a new web form (a form that has never been
    submitted before) or submits the web from with a new login value.
</p>
<p>
    Use the <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.Save" data-throw-if-not-resolved="false"></xref> to save these login and password in the
    <xref href="DotNetBrowser.Passwords.IPasswordStore?text=password+store" data-throw-if-not-resolved="false"></xref>. Stored credentials will be
    shown next time in the suggestions pop-up when focusing
    the input associated with login or password.
</p>
<p>
    Use the <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave" data-throw-if-not-resolved="false"></xref> to blacklist password forms on this
    <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordParameters.Url?text=+URL" data-throw-if-not-resolved="false"></xref>. After this, the handler will never be invoked again until
    you
    <xref href="DotNetBrowser.Passwords.PasswordStoreExtensions.RemoveByUrl(DotNetBrowser.Passwords.IPasswordStore%2cSystem.String)?text=remove" data-throw-if-not-resolved="false"></xref> this blacklisted record from the
    <xref href="DotNetBrowser.Passwords.IPasswordStore?text=+password+store" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    Use the <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.Ignore" data-throw-if-not-resolved="false"></xref> to ignore the suggestion to save the login and
    password in the  <xref href="DotNetBrowser.Passwords.IPasswordStore?text=password+store" data-throw-if-not-resolved="false"></xref>. The handler will be invoked again if
    this or another web form is submitted on the same URL.
</p>
<p>
    The prerequisites for the handler invocation:

<ul><li>The login and password should not be empty.</li><li>The scheme should be web-safe.The list of web-safe schemes: HTTP, HTTPS, WS, and WSS.</li><li>The <xref href="DotNetBrowser.Profile.IProfile?text=profile" data-throw-if-not-resolved="false"></xref> should not be incognito.</li><li>The valid SSL certificate is used.</li><li>A positive server response on the web form submission.</li></ul>
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the response
    <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave" data-throw-if-not-resolved="false"></xref>  will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Passwords_IPasswords_UpdatePasswordHandler"></a> UpdatePasswordHandler

Gets or sets a handler that is used when the user is prompted to update the password in the
<xref href="DotNetBrowser.Passwords.IPasswordStore?text=%0a++++++++++++password+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<UpdatePasswordParameters, UpdatePasswordResponse> UpdatePasswordHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.md), [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md)\>

#### Remarks

<p>
    This handler is equivalent to the "Update Password?" bubble in Chromium.
</p>
<p>
    The handler can be invoked only if the login and password from the form were previously
    <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.Save?text=saved" data-throw-if-not-resolved="false"></xref> in the <xref href="DotNetBrowser.Passwords.IPasswordStore?text=+password+store" data-throw-if-not-resolved="false"></xref>
    and now user entered a new password value.
</p>
<p>
    Use the <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.Update" data-throw-if-not-resolved="false"></xref> method to update the password for this
    <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.Login?text=+login" data-throw-if-not-resolved="false"></xref> in the <xref href="DotNetBrowser.Passwords.IPasswordStore?text=+password+store" data-throw-if-not-resolved="false"></xref>
    .
    The updated password will be reflected in the suggestions pop-up.
</p>
<p>
    Use the <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.Ignore" data-throw-if-not-resolved="false"></xref> method to stay with the old password. If you submit
    the form with the same password value next time the handler will be invoked again.
</p>
<p>
    The prerequisites for the handler invocation:

<ul><li>The password should not be empty.</li><li>The scheme should be web-safe.The list of web-safe schemes: HTTP, HTTPS, WS, and WSS.</li><li>The <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> profile should not be incognito.</li><li>The valid SSL certificate is used.</li><li>A positive server response on the web form submission.</li></ul>
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the response
    <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.Ignore" data-throw-if-not-resolved="false"></xref>  will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> has already been disposed.

