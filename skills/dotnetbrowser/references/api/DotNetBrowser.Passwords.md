# <a id="DotNetBrowser_Passwords"></a> Namespace DotNetBrowser.Passwords

### Namespaces

 [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)

### Classes

 [PasswordRecord.Builder](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord_Builder)

A builder for creating a new <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

 [PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)

A record saved in the <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

 [PasswordStoreExtensions](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordStoreExtensions)

Provides extension methods for <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

### Interfaces

 [IPasswordStore](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_IPasswordStore)

A service that allows working with <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> logins and passwords saved in
the Chromium password store.

 [IPasswords](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_IPasswords)

A service that allows managing passwords.

## <a id="DotNetBrowser_Passwords_PasswordRecord"></a> Class PasswordRecord

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A record saved in the <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class PasswordRecord
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Login"></a> Login

Gets the user's login.

```csharp
public string Login { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    For the blacklisted records the login is empty.
</p>

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Password"></a> Password

Gets the password.

```csharp
public string Password { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    For the blacklisted records the password is empty.
</p>

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Url"></a> Url

Gets the URL of the page where the form was submitted.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    For saved records, this is the full URL of the form page, including the path
    (e.g. <code>https://example.com/login.php</code>).
</p>
<p>
    For blacklisted records (created via <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave" data-throw-if-not-resolved="false"></xref>),
    this is the origin URL containing only the scheme, host, and port
    (e.g. <code>https://example.com/</code>).
</p>

### Methods

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Passwords_PasswordRecord_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Passwords_PasswordRecord_Builder"></a> Class PasswordRecord.Builder

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class PasswordRecord.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordRecord.Builder](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Login"></a> Login

Gets or sets the user's login.

```csharp
public string Login { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Password"></a> Password

Gets or sets the password.

```csharp
public string Password { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Url"></a> Url

Gets or sets the full URL of the page where the form is submitted.

```csharp
public string Url { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Build"></a> Build\(\)

Builds the <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public PasswordRecord Build()
```

##### Returns

 [PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)

A new <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Passwords_PasswordStoreExtensions"></a> Class PasswordStoreExtensions

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

Provides extension methods for <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
public static class PasswordStoreExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordStoreExtensions](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordStoreExtensions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Passwords_PasswordStoreExtensions_RemoveByUrl_DotNetBrowser_Passwords_IPasswordStore_System_String_"></a> RemoveByUrl\(IPasswordStore, string\)

Removes all records associated with the specified URL from the password store.

```csharp
public static void RemoveByUrl(this IPasswordStore store, string url)
```

##### Parameters

`store` [IPasswordStore](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_IPasswordStore)

The password store.

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL associated with the records to remove.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty, or contains only blank characters.

## <a id="DotNetBrowser_Passwords_IPasswordStore"></a> Interface IPasswordStore

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A service that allows working with <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> logins and passwords saved in
the Chromium password store.

```csharp
public interface IPasswordStore
```

##### Extension Methods

[PasswordStoreExtensions.RemoveByUrl\(IPasswordStore, string\)](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordStoreExtensions_RemoveByUrl_DotNetBrowser_Passwords_IPasswordStore_System_String_)

### Properties

#### <a id="DotNetBrowser_Passwords_IPasswordStore_All"></a> All

Gets all records from the password store including
<xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave?text=%0a++++++++++++blacklisted%0a++++++++" data-throw-if-not-resolved="false"></xref>
ones.

```csharp
IReadOnlyList<PasswordRecord> All { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)\>

##### Remarks

The blacklisted entries will have an empty <xref href="DotNetBrowser.Passwords.PasswordRecord.Login" data-throw-if-not-resolved="false"></xref> property.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Passwords_IPasswordStore_AllNeverSaved"></a> AllNeverSaved

Gets only <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave?text=blacklisted" data-throw-if-not-resolved="false"></xref> (marked as "never-saved") records
from the password store.

```csharp
IReadOnlyList<PasswordRecord> AllNeverSaved { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Passwords_IPasswordStore_AllSaved"></a> AllSaved

Gets only <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.Save" data-throw-if-not-resolved="false"></xref> saved records from the password store.

```csharp
IReadOnlyList<PasswordRecord> AllSaved { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Passwords_IPasswordStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated wit this <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

### Methods

#### <a id="DotNetBrowser_Passwords_IPasswordStore_Add_DotNetBrowser_Passwords_PasswordRecord_"></a> Add\(PasswordRecord\)

Adds a record to the password store.

```csharp
void Add(PasswordRecord record)
```

##### Parameters

`record` [PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)

The record to add.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">record</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The password record validation failed.

#### <a id="DotNetBrowser_Passwords_IPasswordStore_Clear"></a> Clear\(\)

Clears all records in the password store.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Passwords_IPasswordStore_Remove_DotNetBrowser_Passwords_PasswordRecord_"></a> Remove\(PasswordRecord\)

Removes a record from the password store.

```csharp
void Remove(PasswordRecord record)
```

##### Parameters

`record` [PasswordRecord](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_PasswordRecord)

The record to remove.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">record</code> is null.

## <a id="DotNetBrowser_Passwords_IPasswords"></a> Interface IPasswords

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing passwords.

```csharp
public interface IPasswords : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Passwords_IPasswords_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Passwords_IPasswords_SavePasswordHandler"></a> SavePasswordHandler

Gets or sets a handler that is used when the user is prompted to save the credentials in the
<xref href="DotNetBrowser.Passwords.IPasswordStore?text=%0a++++++++++++password+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<SavePasswordParameters, SavePasswordResponse> SavePasswordHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordParameters), [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Passwords_IPasswords_UpdatePasswordHandler"></a> UpdatePasswordHandler

Gets or sets a handler that is used when the user is prompted to update the password in the
<xref href="DotNetBrowser.Passwords.IPasswordStore?text=%0a++++++++++++password+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<UpdatePasswordParameters, UpdatePasswordResponse> UpdatePasswordHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters), [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> has already been disposed.
