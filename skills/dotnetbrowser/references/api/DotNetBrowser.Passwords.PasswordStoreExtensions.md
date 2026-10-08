# <a id="DotNetBrowser_Passwords_PasswordStoreExtensions"></a> Class PasswordStoreExtensions

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

Provides extension methods for <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
public static class PasswordStoreExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordStoreExtensions](DotNetBrowser.Passwords.PasswordStoreExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Passwords_PasswordStoreExtensions_RemoveByUrl_DotNetBrowser_Passwords_IPasswordStore_System_String_"></a> RemoveByUrl\(IPasswordStore, string\)

Removes all records associated with the specified URL from the password store.

```csharp
public static void RemoveByUrl(this IPasswordStore store, string url)
```

#### Parameters

`store` [IPasswordStore](DotNetBrowser.Passwords.IPasswordStore.md)

The password store.

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL associated with the records to remove.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty, or contains only blank characters.

