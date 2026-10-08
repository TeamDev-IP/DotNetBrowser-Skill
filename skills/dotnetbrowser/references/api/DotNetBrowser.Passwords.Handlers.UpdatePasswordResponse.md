# <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse"></a> Class UpdatePasswordResponse

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdatePasswordResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse_Ignore"></a> Ignore

Creates a <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser not to update the password
for this <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.Login" data-throw-if-not-resolved="false"></xref>.

```csharp
public static UpdatePasswordResponse Ignore
```

#### Field Value

 [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md)

### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse_Update"></a> Update

Creates a <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to update the password
for this <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.Login" data-throw-if-not-resolved="false"></xref> login in the password store.

```csharp
public static UpdatePasswordResponse Update
```

#### Field Value

 [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md)

