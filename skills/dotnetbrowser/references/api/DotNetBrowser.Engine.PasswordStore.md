# <a id="DotNetBrowser_Engine_PasswordStore"></a> Class PasswordStore

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Defines password store types that are used to specify which encryption storage backend to use to
encrypt cookies on Linux.

```csharp
public sealed class PasswordStore : TypedEnum<string>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Engine_PasswordStore_Auto"></a> Auto

Choose encryption automatically.

```csharp
public static readonly PasswordStore Auto
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_Basic"></a> Basic

Use basic encryption.

```csharp
public static readonly PasswordStore Basic
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_Default"></a> Default

Default password store encryption (Auto).

```csharp
public static readonly PasswordStore Default
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_Gnome"></a> Gnome

Use GNOME encryption.

```csharp
public static readonly PasswordStore Gnome
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_GnomeKeyring"></a> GnomeKeyring

Use GNOME keyring encryption.

```csharp
public static readonly PasswordStore GnomeKeyring
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_GnomeLibsecret"></a> GnomeLibsecret

Use GNOME libsecret encryption.

```csharp
public static readonly PasswordStore GnomeLibsecret
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_KWallet"></a> KWallet

Use KWallet encryption.

```csharp
public static readonly PasswordStore KWallet
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

### <a id="DotNetBrowser_Engine_PasswordStore_KWallet5"></a> KWallet5

Use KWallet5 encryption.

```csharp
public static readonly PasswordStore KWallet5
```

#### Field Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

## Operators

### <a id="DotNetBrowser_Engine_PasswordStore_op_Explicit_System_String__DotNetBrowser_Engine_PasswordStore"></a> explicit operator PasswordStore\(string\)

Returns the <xref href="DotNetBrowser.Engine.PasswordStore" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static explicit operator PasswordStore(string value)
```

#### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The password store string representation

#### Returns

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

The <xref href="DotNetBrowser.Engine.PasswordStore" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.

