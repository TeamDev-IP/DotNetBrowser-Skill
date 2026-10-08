# <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError"></a> Class CertificateVerificationError

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Provides information about an error found by Chromium when verifying an SSL certificate.

```csharp
public sealed class CertificateVerificationError
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CertificateVerificationError](DotNetBrowser.Net.Certificates.CertificateVerificationError.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_DetailedDescription"></a> DetailedDescription

Gets a detailed localized human-friendly description of the verification error.

```csharp
public string DetailedDescription { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>This message is formatted with HTML.</p>

### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_ShortDescription"></a> ShortDescription

Gets a short localized human-friendly description of the verification error.

```csharp
public string ShortDescription { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_VerifyStatus"></a> VerifyStatus

Gets the verification statuses that indicate result
of SSL certificate verification by the Chromium engine.

```csharp
public CertificateVerificationStatus VerifyStatus { get; }
```

#### Property Value

 [CertificateVerificationStatus](DotNetBrowser.Net.Certificates.CertificateVerificationStatus.md)

## Methods

### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

