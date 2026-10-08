# <a id="DotNetBrowser_Passwords_PasswordRecord_Builder"></a> Class PasswordRecord.Builder

Namespace: [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class PasswordRecord.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PasswordRecord.Builder](DotNetBrowser.Passwords.PasswordRecord.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Login"></a> Login

Gets or sets the user's login.

```csharp
public string Login { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Password"></a> Password

Gets or sets the password.

```csharp
public string Password { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Url"></a> Url

Gets or sets the full URL of the page where the form is submitted.

```csharp
public string Url { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Passwords_PasswordRecord_Builder_Build"></a> Build\(\)

Builds the <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public PasswordRecord Build()
```

#### Returns

 [PasswordRecord](DotNetBrowser.Passwords.PasswordRecord.md)

A new <xref href="DotNetBrowser.Passwords.PasswordRecord" data-throw-if-not-resolved="false"></xref> instance.

