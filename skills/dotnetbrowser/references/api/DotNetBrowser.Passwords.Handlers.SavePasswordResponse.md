# <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse"></a> Class SavePasswordResponse

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SavePasswordResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_Ignore"></a> Ignore

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to ignore
credentials saving.

```csharp
public static SavePasswordResponse Ignore
```

#### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)

### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_NeverSave"></a> NeverSave

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser
that password forms on this <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordParameters.Url" data-throw-if-not-resolved="false"></xref> URL should be
blacklisted(marked as "never-saved") and <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>
should not be invoked in the future.

```csharp
public static SavePasswordResponse NeverSave
```

#### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)

### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_Save"></a> Save

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to save
credentials in the store.

```csharp
public static SavePasswordResponse Save
```

#### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)

