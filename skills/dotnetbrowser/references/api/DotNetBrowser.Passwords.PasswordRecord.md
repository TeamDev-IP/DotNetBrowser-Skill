# <a id="DotNetBrowser_Passwords_PasswordRecord"></a> Class PasswordRecord

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A record saved in the <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class PasswordRecord
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Passwords_PasswordRecord_Login"></a> Login

Gets the user's login.

```csharp
public string Login { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    For the blacklisted records the login is empty.
</p>

### <a id="DotNetBrowser_Passwords_PasswordRecord_Password"></a> Password

Gets the password.

```csharp
public string Password { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    For the blacklisted records the password is empty.
</p>

### <a id="DotNetBrowser_Passwords_PasswordRecord_Url"></a> Url

Gets the URL of the page where the form was submitted.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    For saved records, this is the full URL of the form page, including the path
    (e.g. <code>https://example.com/login.php</code>).
</p>
<p>
    For blacklisted records (created via <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse.NeverSave" data-throw-if-not-resolved="false"></xref>),
    this is the origin URL containing only the scheme, host, and port
    (e.g. <code>https://example.com/</code>).
</p>

## Methods

### <a id="DotNetBrowser_Passwords_PasswordRecord_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Passwords_PasswordRecord_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

