# <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage"></a> Class ExtendedKeyUsage

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Defines how the certificate key can be used.

```csharp
public sealed class ExtendedKeyUsage : TypedEnum<string>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_ClientAuth"></a> ClientAuth

Gets the key can be used for TLS WWW client authentication.

```csharp
public static readonly ExtendedKeyUsage ClientAuth
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_CodeSigning"></a> CodeSigning

Gets the key can be used for signing of downloadable executable code.

```csharp
public static readonly ExtendedKeyUsage CodeSigning
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_EmailProtection"></a> EmailProtection

Gets the key can be used for email protection.

```csharp
public static readonly ExtendedKeyUsage EmailProtection
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecEndSystem"></a> IpsecEndSystem

Gets the key can be used for IP security end system.

```csharp
public static readonly ExtendedKeyUsage IpsecEndSystem
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecTunnel"></a> IpsecTunnel

Gets the key can be used for IP security tunnel termination.

```csharp
public static readonly ExtendedKeyUsage IpsecTunnel
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecUser"></a> IpsecUser

Gets the key can be used for IP security user.

```csharp
public static readonly ExtendedKeyUsage IpsecUser
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_OcspSigning"></a> OcspSigning

Gets the key can be used for signing OCSP responses.

```csharp
public static readonly ExtendedKeyUsage OcspSigning
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_ServerAuth"></a> ServerAuth

Gets the key can be used for TLS WWW server authentication.

```csharp
public static readonly ExtendedKeyUsage ServerAuth
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_TimeStamping"></a> TimeStamping

Gets the key can be used for binding the hash of an object to a time.

```csharp
public static readonly ExtendedKeyUsage TimeStamping
```

#### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

## Operators

### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_op_Explicit_System_String__DotNetBrowser_Net_Certificates_ExtendedKeyUsage"></a> explicit operator ExtendedKeyUsage\(string\)

Creates the ExtendedKeysUsage instance from string representation

```csharp
public static explicit operator ExtendedKeyUsage(string str)
```

#### Parameters

`str` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

#### Returns

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)

a corresponding <xref href="DotNetBrowser.Net.Certificates.ExtendedKeyUsage" data-throw-if-not-resolved="false"></xref> instance.

