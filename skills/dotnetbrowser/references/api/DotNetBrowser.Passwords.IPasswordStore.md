# <a id="DotNetBrowser_Passwords_IPasswordStore"></a> Interface IPasswordStore

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A service that allows working with <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> logins and passwords saved in
the Chromium password store.

```csharp
public interface IPasswordStore
```

#### Extension Methods

[PasswordStoreExtensions.RemoveByUrl\(IPasswordStore, string\)](DotNetBrowser.Passwords.PasswordStoreExtensions.md\#DotNetBrowser\_Passwords\_PasswordStoreExtensions\_RemoveByUrl\_DotNetBrowser\_Passwords\_IPasswordStore\_System\_String\_)

## Properties

### <a id="DotNetBrowser_Passwords_IPasswordStore_All"></a> All

Gets all records from the password store including
<xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave?text=%0a++++++++++++blacklisted%0a++++++++" data-throw-if-not-resolved="false"></xref>
ones.

```csharp
IReadOnlyList<PasswordRecord> All { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)\>

#### Remarks

The blacklisted entries will have an empty <xref href="DotNetBrowser.Passwords.PasswordRecord.Login" data-throw-if-not-resolved="false"></xref> property.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Passwords_IPasswordStore_AllNeverSaved"></a> AllNeverSaved

Gets only <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave?text=blacklisted" data-throw-if-not-resolved="false"></xref> (marked as "never-saved") records
from the password store.

```csharp
IReadOnlyList<PasswordRecord> AllNeverSaved { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Passwords_IPasswordStore_AllSaved"></a> AllSaved

Gets only <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.Save" data-throw-if-not-resolved="false"></xref> saved records from the password store.

```csharp
IReadOnlyList<PasswordRecord> AllSaved { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Passwords_IPasswordStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated wit this <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Passwords_IPasswordStore_Add_DotNetBrowser_Passwords_PasswordRecord_"></a> Add\(PasswordRecord\)

Adds a record to the password store.

```csharp
void Add(PasswordRecord record)
```

#### Parameters

`record` [PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)

The record to add.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">record</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The password record validation failed.

### <a id="DotNetBrowser_Passwords_IPasswordStore_Clear"></a> Clear\(\)

Clears all records in the password store.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Passwords_IPasswordStore_Remove_DotNetBrowser_Passwords_PasswordRecord_"></a> Remove\(PasswordRecord\)

Removes a record from the password store.

```csharp
void Remove(PasswordRecord record)
```

#### Parameters

`record` [PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)

The record to remove.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">record</code> is null.

