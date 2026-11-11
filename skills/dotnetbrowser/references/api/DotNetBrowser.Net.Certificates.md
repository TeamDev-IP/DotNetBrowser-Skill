# <a id="DotNetBrowser_Net_Certificates"></a> Namespace DotNetBrowser.Net.Certificates

### Classes

 [Certificate](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_Certificate)

Provides information about the digital certificate. This certificate represents a X.509 certificate,
which consists of a particular identity or end-entity certificate, such as an server
identity or a client public key certificate, and zero or more intermediate certificates.

 [CertificateVerificationError](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationError)

Provides information about an error found by Chromium when verifying an SSL certificate.

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

Defines how the certificate key can be used.

### Enums

 [CertificateVerificationStatus](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationStatus)

The status that indicates result of SSL certificate verification
by default Chromium certificate verifier.

## <a id="DotNetBrowser_Net_Certificates_Certificate"></a> Class Certificate

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Provides information about the digital certificate. This certificate represents a X.509 certificate,
which consists of a particular identity or end-entity certificate, such as an server
identity or a client public key certificate, and zero or more intermediate certificates.

```csharp
public sealed class Certificate
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Certificate](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_Certificate)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_Certificates_Certificate__ctor_System_Security_Cryptography_X509Certificates_X509Certificate_"></a> Certificate\(X509Certificate\)

Constructs a new Certificate instance from an X509Certificate.

```csharp
public Certificate(X509Certificate certificate)
```

##### Parameters

`certificate` [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

the certificate.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when value is null.

#### <a id="DotNetBrowser_Net_Certificates_Certificate__ctor_System_Security_Cryptography_X509Certificates_X509Certificate_System_Security_Cryptography_X509Certificates_X509CertificateCollection_"></a> Certificate\(X509Certificate, X509CertificateCollection\)

Constructs a new Certificate instance from an X509Certificate and the list of
intermediate X.509 certificates associated with this the certificate that may be needed for
chain building.

```csharp
public Certificate(X509Certificate certificate, X509CertificateCollection intermediateCertificates)
```

##### Parameters

`certificate` [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

The X.509 certificate

`intermediateCertificates` [X509CertificateCollection](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificatecollection)

The intermediate X.509 certificates associated with this the certificate.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when certificate or intermediate certificates are null.

### Properties

#### <a id="DotNetBrowser_Net_Certificates_Certificate_CaFingerPrint"></a> CaFingerPrint

The CA Fingerprint of certificate.

```csharp
public string CaFingerPrint { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_Expired"></a> Expired

Indicates whether the certificate has already expired.

```csharp
public bool Expired { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_ExtendedKeyUsages"></a> ExtendedKeyUsages

A collection of extended key usages. This collection can be empty if the
extended key usages info was not extracted from certificate because of corrupt data.

```csharp
public IEnumerable<ExtendedKeyUsage> ExtendedKeyUsages { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)\>

#### <a id="DotNetBrowser_Net_Certificates_Certificate_Fingerprint"></a> Fingerprint

A certificate fingerprint. Can be an empty string if the fingerprint was not extracted
from certificate because of corrupt data.

```csharp
public string Fingerprint { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_IntermediateCertificates"></a> IntermediateCertificates

Gets the list of intermediate certificates associated with this certificate that may be
needed for chain building.

```csharp
public IReadOnlyList<Certificate> IntermediateCertificates { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Certificate](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_Certificate)\>

#### <a id="DotNetBrowser_Net_Certificates_Certificate_Issuer"></a> Issuer

The Issuer entity of certificate. Can be null if the issuer was not extracted
from certificate because of corrupt certificate data.

```csharp
public string Issuer { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_IssuerName"></a> IssuerName

The name of the issuer of the certificate.

```csharp
public string IssuerName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_KeyUsages"></a> KeyUsages

The key usages as a combination of flags. Can be null if the key usages info
was not extracted from the certificate because of corrupt data.

```csharp
public X509KeyUsageFlags? KeyUsages { get; }
```

##### Property Value

 [X509KeyUsageFlags](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509keyusageflags)?

#### <a id="DotNetBrowser_Net_Certificates_Certificate_NotAfter"></a> NotAfter

The DateTime that describes until what time the certificate is valid.

```csharp
public DateTime NotAfter { get; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_NotBefore"></a> NotBefore

The DateTime starting from the certificate is valid.

```csharp
public DateTime NotBefore { get; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_SerialNumber"></a> SerialNumber

The serial number of certificate. Can be an empty string if the serial
number was not extracted from certificate because of corrupt data.

```csharp
public string SerialNumber { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_Subject"></a> Subject

The Subject entity of certificate. Can be null if the subject
was not extracted from certificate data because of corrupt certificate data.

```csharp
public string Subject { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_SubjectName"></a> SubjectName

The name of the subject of the certificate. For HTTPS server certificates, this
represents the web server. The common name of the subject should match the host name of the web server.

```csharp
public string SubjectName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_X509Certificate"></a> X509Certificate

The X509Certificate that provides access to all certificate information.
Can be null if the information was not extracted because of corrupt certificate data.

```csharp
public X509Certificate X509Certificate { get; }
```

##### Property Value

 [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

#### <a id="DotNetBrowser_Net_Certificates_Certificate_X509Certificate2"></a> X509Certificate2

The X509Certificate2 that provides access to all certificate information.
Can be null if the information was not extracted because of corrupt certificate data.

```csharp
public X509Certificate2 X509Certificate2 { get; }
```

##### Property Value

 [X509Certificate2](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate2)

### Methods

#### <a id="DotNetBrowser_Net_Certificates_Certificate_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError"></a> Class CertificateVerificationError

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Provides information about an error found by Chromium when verifying an SSL certificate.

```csharp
public sealed class CertificateVerificationError
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CertificateVerificationError](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationError)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_DetailedDescription"></a> DetailedDescription

Gets a detailed localized human-friendly description of the verification error.

```csharp
public string DetailedDescription { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>This message is formatted with HTML.</p>

#### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_ShortDescription"></a> ShortDescription

Gets a short localized human-friendly description of the verification error.

```csharp
public string ShortDescription { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_VerifyStatus"></a> VerifyStatus

Gets the verification statuses that indicate result
of SSL certificate verification by the Chromium engine.

```csharp
public CertificateVerificationStatus VerifyStatus { get; }
```

##### Property Value

 [CertificateVerificationStatus](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_CertificateVerificationStatus)

### Methods

#### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_Certificates_CertificateVerificationError_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage"></a> Class ExtendedKeyUsage

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Defines how the certificate key can be used.

```csharp
public sealed class ExtendedKeyUsage : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_ClientAuth"></a> ClientAuth

Gets the key can be used for TLS WWW client authentication.

```csharp
public static readonly ExtendedKeyUsage ClientAuth
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_CodeSigning"></a> CodeSigning

Gets the key can be used for signing of downloadable executable code.

```csharp
public static readonly ExtendedKeyUsage CodeSigning
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_EmailProtection"></a> EmailProtection

Gets the key can be used for email protection.

```csharp
public static readonly ExtendedKeyUsage EmailProtection
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecEndSystem"></a> IpsecEndSystem

Gets the key can be used for IP security end system.

```csharp
public static readonly ExtendedKeyUsage IpsecEndSystem
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecTunnel"></a> IpsecTunnel

Gets the key can be used for IP security tunnel termination.

```csharp
public static readonly ExtendedKeyUsage IpsecTunnel
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_IpsecUser"></a> IpsecUser

Gets the key can be used for IP security user.

```csharp
public static readonly ExtendedKeyUsage IpsecUser
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_OcspSigning"></a> OcspSigning

Gets the key can be used for signing OCSP responses.

```csharp
public static readonly ExtendedKeyUsage OcspSigning
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_ServerAuth"></a> ServerAuth

Gets the key can be used for TLS WWW server authentication.

```csharp
public static readonly ExtendedKeyUsage ServerAuth
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_TimeStamping"></a> TimeStamping

Gets the key can be used for binding the hash of an object to a time.

```csharp
public static readonly ExtendedKeyUsage TimeStamping
```

##### Field Value

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

### Operators

#### <a id="DotNetBrowser_Net_Certificates_ExtendedKeyUsage_op_Explicit_System_String__DotNetBrowser_Net_Certificates_ExtendedKeyUsage"></a> explicit operator ExtendedKeyUsage\(string\)

Creates the ExtendedKeysUsage instance from string representation

```csharp
public static explicit operator ExtendedKeyUsage(string str)
```

##### Parameters

`str` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

##### Returns

 [ExtendedKeyUsage](DotNetBrowser.Net.Certificates.md#DotNetBrowser_Net_Certificates_ExtendedKeyUsage)

a corresponding <xref href="DotNetBrowser.Net.Certificates.ExtendedKeyUsage" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Net_Certificates_CertificateVerificationStatus"></a> Enum CertificateVerificationStatus

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

The status that indicates result of SSL certificate verification
by default Chromium certificate verifier.

```csharp
public enum CertificateVerificationStatus
```

### Fields

`AuthorityInvalid = 3` 





`CertificateTransparencyRequired = 18` 





`CommonNameInvalid = 1` 





`CtComplianceFailed = 17` 





`DateInvalid = 2` 





`Invalid = 7` 





`IsEv = 14` 





`NameConstraintViolation = 12` 





`NoRevocationMechanism = 4` 





`NonUniqueName = 9` 





`PinnedKeyMissing = 11` 





`RevCheckingEnabled = 15` 





`Revoked = 6` 





`Sha1SignaturePresent = 16` 





`UnableToCheckRevocation = 5` 





`ValidityTooLong = 13` 





`WeakKey = 10` 





`WeakSignatureAlgorithm = 8` 
