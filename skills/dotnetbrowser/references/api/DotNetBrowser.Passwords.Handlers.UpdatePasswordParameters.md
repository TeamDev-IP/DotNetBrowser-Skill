# <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters"></a> Class UpdatePasswordParameters

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdatePasswordParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters_Login"></a> Login

Gets the login for which the password is updated.

```csharp
public string Login { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters_Url"></a> Url

Gets the URL of the resource where the form is located.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

