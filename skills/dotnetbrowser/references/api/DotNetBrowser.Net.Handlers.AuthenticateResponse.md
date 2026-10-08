# <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse"></a> Class AuthenticateResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AuthenticateResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AuthenticateResponse](DotNetBrowser.Net.Handlers.AuthenticateResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Password"></a> Password

Gets the password that will be used for authenticating on a server or a proxy.

```csharp
public string Password { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Username"></a> Username

Gets the username that will be used for authenticating on a server or a proxy.

```csharp
public string Username { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> that cancels authentication process.

```csharp
public static AuthenticateResponse Cancel()
```

#### Returns

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.AuthenticateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Continue_System_String_System_String_"></a> Continue\(string, string\)

Creates a <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> that continues authentication
process with the specified credentials.

```csharp
public static AuthenticateResponse Continue(string username, string password)
```

#### Parameters

`username` [string](https://learn.microsoft.com/dotnet/api/system.string)

Username used for authentication

`password` [string](https://learn.microsoft.com/dotnet/api/system.string)

Password used for authentication

#### Returns

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.AuthenticateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref> implementation.

