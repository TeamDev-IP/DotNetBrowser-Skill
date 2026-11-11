# <a id="DotNetBrowser_Passwords_Handlers"></a> Namespace DotNetBrowser.Passwords.Handlers

### Classes

 [SavePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordParameters)

The parameters of the <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>.

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>.

 [UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters)

The parameters of the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

 [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse)

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Passwords_Handlers_SavePasswordParameters"></a> Class SavePasswordParameters

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SavePasswordParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordParameters_Login"></a> Login

Gets the login value passed in the form.

```csharp
public string Login { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordParameters_Url"></a> Url

Gets the URL of the resource where the form is located.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse"></a> Class SavePasswordResponse

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SavePasswordResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_Ignore"></a> Ignore

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to ignore
credentials saving.

```csharp
public static SavePasswordResponse Ignore
```

##### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)

#### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_NeverSave"></a> NeverSave

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser
that password forms on this <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordParameters.Url" data-throw-if-not-resolved="false"></xref> URL should be
blacklisted(marked as "never-saved") and <xref href="DotNetBrowser.Passwords.IPasswords.SavePasswordHandler" data-throw-if-not-resolved="false"></xref>
should not be invoked in the future.

```csharp
public static SavePasswordResponse NeverSave
```

##### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)

#### <a id="DotNetBrowser_Passwords_Handlers_SavePasswordResponse_Save"></a> Save

Creates a <xref href="DotNetBrowser.Passwords.Handlers.SavePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to save
credentials in the store.

```csharp
public static SavePasswordResponse Save
```

##### Field Value

 [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordResponse)

## <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters"></a> Class UpdatePasswordParameters

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdatePasswordParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters_Login"></a> Login

Gets the login for which the password is updated.

```csharp
public string Login { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters_Url"></a> Url

Gets the URL of the resource where the form is located.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse"></a> Class UpdatePasswordResponse

Namespace: [DotNetBrowser.Passwords.Handlers](DotNetBrowser.Passwords.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Passwords.IPasswords.UpdatePasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UpdatePasswordResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse_Ignore"></a> Ignore

Creates a <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser not to update the password
for this <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.Login" data-throw-if-not-resolved="false"></xref>.

```csharp
public static UpdatePasswordResponse Ignore
```

##### Field Value

 [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse)

#### <a id="DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse_Update"></a> Update

Creates a <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to update the password
for this <xref href="DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.Login" data-throw-if-not-resolved="false"></xref> login in the password store.

```csharp
public static UpdatePasswordResponse Update
```

##### Field Value

 [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordResponse)
