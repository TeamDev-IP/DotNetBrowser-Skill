# <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters"></a> Class AuthenticateParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.AuthenticateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class AuthenticateParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[AuthenticateParameters](DotNetBrowser.Net.Handlers.AuthenticateParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Host"></a> Host

Gets the host of the service issuing the authentication challenge.

```csharp
public string Host { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_IsProxy"></a> IsProxy

Indicates whether this authentication challenge came from a server or a proxy.

```csharp
public bool IsProxy { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Port"></a> Port

Gets the port of the service issuing the authentication challenge.

```csharp
public int Port { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Realm"></a> Realm

Gets the realm of the authentication challenge. This method can return empty string.

```csharp
public string Realm { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Scheme"></a> Scheme

Gets the authentication scheme used, such as "basic" or "digest". In case of FTP server, this method returns empty
string.

```csharp
public string Scheme { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_Url"></a> Url

Gets the URL of a web page that causes authentication.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Net_Handlers_AuthenticateParameters_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

