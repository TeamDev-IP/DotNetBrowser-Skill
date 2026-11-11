# <a id="DotNetBrowser_Net_Handlers"></a> Namespace DotNetBrowser.Net.Handlers

### Classes

 [AuthenticateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

 [CanAccessFileParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

 [CanAccessFileResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

 [CanGetCookiesParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

 [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

 [CanSetCookieParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

 [CanSetCookieResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

 [InterceptRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestParameters)

The parameters of the scheme handler.

 [InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)

A response for the scheme handler.

 [NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters)

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters.

 [ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

 [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersResponse)

The response for the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

 [SendUploadDataParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The response for the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

 [SendUrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref>.

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)

A response of the <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref>.

 [StartTransactionParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

 [StartTransactionResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

 [UrlRequestJobOptions](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestJobOptions)

The options needed to create the <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

 [UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters)

The base class for all the <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters containing
<xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref>.

 [VerifyCertificateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateParameters)

The parameters of the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>.

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

A response for the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>

### Enums

 [ResourceType](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ResourceType)

The type of the resource being loaded.

## <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters"></a> Class AuthenticateParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AuthenticateParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[AuthenticateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Host"></a> Host

Gets the host of the service issuing the authentication challenge.

```csharp
public string Host { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_IsProxy"></a> IsProxy

Indicates whether this authentication challenge came from a server or a proxy.

```csharp
public bool IsProxy { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Port"></a> Port

Gets the port of the service issuing the authentication challenge.

```csharp
public int Port { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Realm"></a> Realm

Gets the realm of the authentication challenge. This method can return empty string.

```csharp
public string Realm { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Scheme"></a> Scheme

Gets the authentication scheme used, such as "basic" or "digest". In case of FTP server, this method returns empty
string.

```csharp
public string Scheme { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Url"></a> Url

Gets the URL of a web page that causes authentication.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse"></a> Class AuthenticateResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AuthenticateResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[AuthenticateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Password"></a> Password

Gets the password that will be used for authenticating on a server or a proxy.

```csharp
public string Password { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Username"></a> Username

Gets the username that will be used for authenticating on a server or a proxy.

```csharp
public string Username { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> that cancels authentication process.

```csharp
public static AuthenticateResponse Cancel()
```

##### Returns

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateResponse)

The <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_AuthenticateResponse_Continue_System_String_System_String_"></a> Continue\(string, string\)

Creates a <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> that continues authentication
process with the specified credentials.

```csharp
public static AuthenticateResponse Continue(string username, string password)
```

##### Parameters

`username` [string](https://learn.microsoft.com/dotnet/api/system.string)

Username used for authentication

`password` [string](https://learn.microsoft.com/dotnet/api/system.string)

Password used for authentication

##### Returns

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateResponse)

The <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_CanAccessFileParameters"></a> Class CanAccessFileParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanAccessFileParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[CanAccessFileParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_CanAccessFileParameters_AbsolutePath"></a> AbsolutePath

Gets the absolute path to the file the request would like to access. On Linux and
macOS returns the path after resolving all symbolic links. On Windows, if the requested
file is a shortcut, the callback will be invoked twice: once for the shortcut, and once
for the destination file path.

```csharp
public string AbsolutePath { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse"></a> Class CanAccessFileResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanAccessFileResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanAccessFileResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse_Can"></a> Can\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> that allows access to the file.

```csharp
public static CanAccessFileResponse Can()
```

##### Returns

 [CanAccessFileResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse_Cannot"></a> Cannot\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> that denies access to the file.

```csharp
public static CanAccessFileResponse Cannot()
```

##### Returns

 [CanAccessFileResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters"></a> Class CanGetCookiesParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanGetCookiesParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters_Cookies"></a> Cookies

Gets a collection of cookies that are going to be sent with the URL request.

```csharp
public IEnumerable<Cookie> Cookies { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)\>

#### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesParameters_Url"></a> Url

Gets the URL associated with the cookies.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse"></a> Class CanGetCookiesResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanGetCookiesResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanGetCookiesResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse_Allow"></a> Allow\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that
allows sending cookies back to web server.

```csharp
public static CanGetCookiesResponse Allow()
```

##### Returns

 [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_CanGetCookiesResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that
denies sending cookies back to web server.

```csharp
public static CanGetCookiesResponse Deny()
```

##### Returns

 [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanGetCookiesHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters"></a> Class CanSetCookieParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanSetCookieParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[CanSetCookieParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters_Cookie"></a> Cookie

Gets the cookie received from the web server.

```csharp
public Cookie Cookie { get; }
```

##### Property Value

 [Cookie](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_Cookie)

#### <a id="DotNetBrowser_Net_Handlers_CanSetCookieParameters_Url"></a> Url

Gets the URL associated with the cookie.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse"></a> Class CanSetCookieResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class CanSetCookieResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanSetCookieResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse_Allow"></a> Allow\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> that allows saving the cookie.

```csharp
public static CanSetCookieResponse Allow()
```

##### Returns

 [CanSetCookieResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_CanSetCookieResponse_Deny"></a> Deny\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> that denies saving the cookie.

```csharp
public static CanSetCookieResponse Deny()
```

##### Returns

 [CanSetCookieResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieResponse)

The <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanSetCookieHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters"></a> Class InterceptRequestParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the scheme handler.

```csharp
public sealed class InterceptRequestParameters : UrlRequestParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters) ← 
[InterceptRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestParameters)

##### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters_Headers"></a> Headers

Gets the collection of HTTP headers sent in the scope of the request.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)\>

#### <a id="DotNetBrowser_Net_Handlers_InterceptRequestParameters_UploadData"></a> UploadData

Gets the data uploaded in the scope of the request.

```csharp
public IUploadData UploadData { get; }
```

##### Property Value

 [IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

## <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse"></a> Class InterceptRequestResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the scheme handler.

```csharp
public sealed class InterceptRequestResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse_Intercept_DotNetBrowser_Net_UrlRequestJob_"></a> Intercept\(UrlRequestJob\)

Creates a <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance indicating that
the request should be intercepted.

```csharp
public static InterceptRequestResponse Intercept(UrlRequestJob job)
```

##### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse.UrlRequestJob" data-throw-if-not-resolved="false"></xref> providing data of the HTTP response
that can be created using the <xref href="DotNetBrowser.Net.INetwork.CreateUrlRequestJob(DotNetBrowser.Net.UrlRequest%2cDotNetBrowser.Net.Handlers.UrlRequestJobOptions)" data-throw-if-not-resolved="false"></xref> method.

##### Returns

 [InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in handler implementation.

#### <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance indicating that
the request should be handled by the Chromium engine.

```csharp
public static InterceptRequestResponse Proceed()
```

##### Returns

 [InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in the scheme handler implementation.

## <a id="DotNetBrowser_Net_Handlers_NetworkParameters"></a> Class NetworkParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters.

```csharp
public class NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters)

##### Derived

[AuthenticateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateParameters), 
[CanAccessFileParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileParameters), 
[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesParameters), 
[CanSetCookieParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieParameters), 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters), 
[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_NetworkParameters_Network"></a> Network

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public INetwork Network { get; }
```

##### Property Value

 [INetwork](DotNetBrowser.Net.md#DotNetBrowser_Net_INetwork)

## <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters"></a> Class ReceiveHeadersParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ReceiveHeadersParameters : UrlRequestParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters) ← 
[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersParameters)

##### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_Charset"></a> Charset

Gets the charset in lower case from the headers. If there's no charset,
returns empty string.

```csharp
public string Charset { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_ContentLength"></a> ContentLength

Gets the number of the content length.

```csharp
public long ContentLength { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_Headers"></a> Headers

Gets the collection of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)\>

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_MimeType"></a> MimeType

Gets the MIME type in lower case from the headers. If there's no MIME
type, returns empty string.

```csharp
public MimeType MimeType { get; }
```

##### Property Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_StatusLine"></a> StatusLine

Gets the first line of a Response message which is the StatusLine,
consisting of the protocol version followed by a numeric status code
and its associated textual phrase.

```csharp
public string StatusLine { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_StatusText"></a> StatusText

Gets the status text.

```csharp
public string StatusText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse"></a> Class ReceiveHeadersResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response for the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ReceiveHeadersResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_HttpHeaders"></a> HttpHeaders

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> HttpHeaders { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)\>

### Methods

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> that uses headers without modification.

```csharp
public static ReceiveHeadersResponse Continue()
```

##### Returns

 [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersResponse)

The <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_OverrideHeaders_System_Collections_Generic_IEnumerable_DotNetBrowser_Net_HttpHeader__"></a> OverrideHeaders\(IEnumerable<HttpHeader\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> that overrides the received headers.

```csharp
public static ReceiveHeadersResponse OverrideHeaders(IEnumerable<HttpHeader> httpHeaders)
```

##### Parameters

`httpHeaders` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)\>

HttpHeaders used for overriding

##### Returns

 [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersResponse)

The <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_SendUploadDataParameters"></a> Class SendUploadDataParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUploadDataParameters : UrlRequestParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters) ← 
[SendUploadDataParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataParameters)

##### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataParameters_UploadData"></a> UploadData

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header.If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

```csharp
public IUploadData UploadData { get; }
```

##### Property Value

 [IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

## <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse"></a> Class SendUploadDataResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response for the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUploadDataResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_UploadData"></a> UploadData

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header.If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

```csharp
public IUploadData UploadData { get; }
```

##### Property Value

 [IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that uses the original upload data.

```csharp
public static SendUploadDataResponse Continue()
```

##### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_BytesData_"></a> Override\(BytesData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(BytesData uploadData)
```

##### Parameters

`uploadData` [BytesData](DotNetBrowser.Net.md#DotNetBrowser_Net_BytesData)

ByteData used for overriding

##### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_TextData_"></a> Override\(TextData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(TextData uploadData)
```

##### Parameters

`uploadData` [TextData](DotNetBrowser.Net.md#DotNetBrowser_Net_TextData)

TextData used for overriding

##### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_FormData_"></a> Override\(FormData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(FormData uploadData)
```

##### Parameters

`uploadData` [FormData](DotNetBrowser.Net.md#DotNetBrowser_Net_FormData)

FormData used for overriding

##### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_MultipartFormData_"></a> Override\(MultipartFormData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(MultipartFormData uploadData)
```

##### Parameters

`uploadData` [MultipartFormData](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormData)

MultipartFormData used for overriding

##### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_SendUrlRequestParameters"></a> Class SendUrlRequestParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUrlRequestParameters : UrlRequestParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters) ← 
[SendUrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestParameters)

##### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestParameters_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance that initiated this request.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

## <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse"></a> Class SendUrlRequestResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response of the <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUrlRequestResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_UrlToRequest"></a> UrlToRequest

Gets the new URL to request.

```csharp
public string UrlToRequest { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
cancels loading process with the <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> code.

```csharp
public static SendUrlRequestResponse Cancel()
```

##### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
continues loading process with the requested URL.

```csharp
public static SendUrlRequestResponse Continue()
```

##### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Override_System_String_"></a> Override\(string\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
overrides the requested URL.

```csharp
public static SendUrlRequestResponse Override(string url)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

New URL used for override

##### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_StartTransactionParameters"></a> Class StartTransactionParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartTransactionParameters : UrlRequestParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters) ← 
[StartTransactionParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionParameters)

##### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_StartTransactionParameters_Headers"></a> Headers

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)\>

## <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse"></a> Class StartTransactionResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartTransactionResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartTransactionResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_HttpHeaders"></a> HttpHeaders

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> HttpHeaders { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)\>

### Methods

#### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> that starts the transaction
with the original headers.

```csharp
public static StartTransactionResponse Continue()
```

##### Returns

 [StartTransactionResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionResponse)

The <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_OverrideHeaders_System_Collections_Generic_IEnumerable_DotNetBrowser_Net_HttpHeader__"></a> OverrideHeaders\(IEnumerable<HttpHeader\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> that overrides
headers and starts the transaction

```csharp
public static StartTransactionResponse OverrideHeaders(IEnumerable<HttpHeader> httpHeaders)
```

##### Parameters

`httpHeaders` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)\>

HttpHeaders used for overriding

##### Returns

 [StartTransactionResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionResponse)

The <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions"></a> Class UrlRequestJobOptions

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The options needed to create the <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class UrlRequestJobOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJobOptions](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestJobOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions_Headers"></a> Headers

Gets or sets the list of the HTTP headers that will be a part of the response.

```csharp
public List<HttpHeader> Headers { get; set; }
```

##### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)\>

#### <a id="DotNetBrowser_Net_Handlers_UrlRequestJobOptions_HttpStatusCode"></a> HttpStatusCode

Gets or sets the HTTP status code of the response.

```csharp
public HttpStatusCode HttpStatusCode { get; set; }
```

##### Property Value

 [HttpStatusCode](https://learn.microsoft.com/dotnet/api/system.net.httpstatuscode)

## <a id="DotNetBrowser_Net_Handlers_UrlRequestParameters"></a> Class UrlRequestParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all the <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref>-related handlers parameters containing
<xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UrlRequestParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestParameters)

##### Derived

[InterceptRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestParameters), 
[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersParameters), 
[SendUploadDataParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataParameters), 
[SendUrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestParameters), 
[StartTransactionParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_UrlRequestParameters_UrlRequest"></a> UrlRequest

The URL request received from the Chromium engine.

```csharp
public UrlRequest UrlRequest { get; }
```

##### Property Value

 [UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

## <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters"></a> Class VerifyCertificateParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class VerifyCertificateParameters : NetworkParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters) ← 
[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateParameters)

##### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_NetworkParameters_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_Certificate"></a> Certificate

Gets the SSL certificate to verify.

```csharp
public Certificate Certificate { get; }
```

##### Property Value

 [Certificate](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_Certificate)

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_HostName"></a> HostName

Gets the SSL server host name.

```csharp
public string HostName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_VerifyErrors"></a> VerifyErrors

Gets the verification errors that indicate result
of SSL certificate verification by the Chromium engine.
If this collection is empty, then default SSL certificate verifier couldn't find any issues with the
given certificate, so it's a valid certificate.

```csharp
public IEnumerable<CertificateVerificationError> VerifyErrors { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[CertificateVerificationError](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationError)\>

## <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse"></a> Class VerifyCertificateResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>

```csharp
public sealed class VerifyCertificateResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Default"></a> Default\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that lets Chromium decide
whether SSL certificate should be accepted or rejected.

```csharp
public static VerifyCertificateResponse Default()
```

##### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Invalid"></a> Invalid\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine
that the given certificate is invalid with the <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus.Invalid" data-throw-if-not-resolved="false"></xref>.

```csharp
public static VerifyCertificateResponse Invalid()
```

##### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Invalid_System_Collections_Generic_IList_DotNetBrowser_Net_Certificates_CertificateVerificationStatus__"></a> Invalid\(IList<CertificateVerificationStatus\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine
that the given certificate is invalid with the specific <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus" data-throw-if-not-resolved="false"></xref>.

```csharp
public static VerifyCertificateResponse Invalid(IList<CertificateVerificationStatus> certificateVerificationStatuses)
```

##### Parameters

`certificateVerificationStatuses` [IList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ilist\-1)<[CertificateVerificationStatus](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationStatus)\>

The list of statuses that explain why the certificate is invalid.

##### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Remarks

<p>
    If the status list is null or empty the <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus.Invalid" data-throw-if-not-resolved="false"></xref> value will
    be used.
</p>

#### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Valid"></a> Valid\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that marks SSL certificate
as valid and must be accepted.

```csharp
public static VerifyCertificateResponse Valid()
```

##### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Net_Handlers_ResourceType"></a> Enum ResourceType

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The type of the resource being loaded.

```csharp
public enum ResourceType
```

### Fields

`CspReport = 17` 

The Content Security Policy report.



`Favicon = 13` 

A favicon.



`FontResource = 6` 

A font.



`Image = 5` 

An image (jpg/gif/png/etc).



`Json = 21` 

The JSON resource.



`MainFrame = 1` 

Top level page.



`Media = 9` 

A media resource.



`Object = 8` 

An object (or embed) tag for a plugin, or a resource that a plugin requested.



`Ping = 15` 

A ping request for &lt;a ping&gt;.



`PluginResource = 18` 

The main plugin resource.



`Prefetch = 12` 

An explicitly requested prefetch.



`PreloadMainFrame = 19` 

The preloaded main frame.



`PreloadSubFrame = 20` 

The preloaded sub frame.



`Script = 4` 

An external script.



`ServiceWorker = 16` 

The main resource of a service worker.



`SharedWorker = 11` 

The main resource of a shared worker.



`Stylesheet = 3` 

A CSS stylesheet.



`SubFrame = 2` 

Frame or IFRAME.



`SubResource = 7` 

An "other" sub-resource.



`Worker = 10` 

The main resource of a dedicated worker.



`Xhr = 14` 

A XMLHttpRequest.
