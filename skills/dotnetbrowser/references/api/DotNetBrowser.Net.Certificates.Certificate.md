# <a id="DotNetBrowser_Net_Certificates_Certificate"></a> Class Certificate

Namespace: [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)  
Assembly: DotNetBrowser.dll  

Provides information about the digital certificate. This certificate represents a X.509 certificate,
which consists of a particular identity or end-entity certificate, such as an server
identity or a client public key certificate, and zero or more intermediate certificates.

```csharp
public sealed class Certificate
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Certificate](DotNetBrowser.Net.Certificates.Certificate.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_Certificates_Certificate__ctor_System_Security_Cryptography_X509Certificates_X509Certificate_"></a> Certificate\(X509Certificate\)

Constructs a new Certificate instance from an X509Certificate.

```csharp
public Certificate(X509Certificate certificate)
```

#### Parameters

`certificate` [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

the certificate.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when value is null.

### <a id="DotNetBrowser_Net_Certificates_Certificate__ctor_System_Security_Cryptography_X509Certificates_X509Certificate_System_Security_Cryptography_X509Certificates_X509CertificateCollection_"></a> Certificate\(X509Certificate, X509CertificateCollection\)

Constructs a new Certificate instance from an X509Certificate and the list of
intermediate X.509 certificates associated with this the certificate that may be needed for
chain building.

```csharp
public Certificate(X509Certificate certificate, X509CertificateCollection intermediateCertificates)
```

#### Parameters

`certificate` [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

The X.509 certificate

`intermediateCertificates` [X509CertificateCollection](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificatecollection)

The intermediate X.509 certificates associated with this the certificate.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when certificate or intermediate certificates are null.

## Properties

### <a id="DotNetBrowser_Net_Certificates_Certificate_CaFingerPrint"></a> CaFingerPrint

The CA Fingerprint of certificate.

```csharp
public string CaFingerPrint { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_Expired"></a> Expired

Indicates whether the certificate has already expired.

```csharp
public bool Expired { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_Certificates_Certificate_ExtendedKeyUsages"></a> ExtendedKeyUsages

A collection of extended key usages. This collection can be empty if the
extended key usages info was not extracted from certificate because of corrupt data.

```csharp
public IEnumerable<ExtendedKeyUsage> ExtendedKeyUsages { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[ExtendedKeyUsage](DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md)\>

### <a id="DotNetBrowser_Net_Certificates_Certificate_Fingerprint"></a> Fingerprint

A certificate fingerprint. Can be an empty string if the fingerprint was not extracted
from certificate because of corrupt data.

```csharp
public string Fingerprint { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_IntermediateCertificates"></a> IntermediateCertificates

Gets the list of intermediate certificates associated with this certificate that may be
needed for chain building.

```csharp
public IReadOnlyList<Certificate> IntermediateCertificates { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Certificate](DotNetBrowser.Net.Certificates.Certificate.md)\>

### <a id="DotNetBrowser_Net_Certificates_Certificate_Issuer"></a> Issuer

The Issuer entity of certificate. Can be null if the issuer was not extracted
from certificate because of corrupt certificate data.

```csharp
public string Issuer { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_IssuerName"></a> IssuerName

The name of the issuer of the certificate.

```csharp
public string IssuerName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_KeyUsages"></a> KeyUsages

The key usages as a combination of flags. Can be null if the key usages info
was not extracted from the certificate because of corrupt data.

```csharp
public X509KeyUsageFlags? KeyUsages { get; }
```

#### Property Value

 [X509KeyUsageFlags](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509keyusageflags)?

### <a id="DotNetBrowser_Net_Certificates_Certificate_NotAfter"></a> NotAfter

The DateTime that describes until what time the certificate is valid.

```csharp
public DateTime NotAfter { get; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

### <a id="DotNetBrowser_Net_Certificates_Certificate_NotBefore"></a> NotBefore

The DateTime starting from the certificate is valid.

```csharp
public DateTime NotBefore { get; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)

### <a id="DotNetBrowser_Net_Certificates_Certificate_SerialNumber"></a> SerialNumber

The serial number of certificate. Can be an empty string if the serial
number was not extracted from certificate because of corrupt data.

```csharp
public string SerialNumber { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_Subject"></a> Subject

The Subject entity of certificate. Can be null if the subject
was not extracted from certificate data because of corrupt certificate data.

```csharp
public string Subject { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_SubjectName"></a> SubjectName

The name of the subject of the certificate. For HTTPS server certificates, this
represents the web server. The common name of the subject should match the host name of the web server.

```csharp
public string SubjectName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Certificates_Certificate_X509Certificate"></a> X509Certificate

The X509Certificate that provides access to all certificate information.
Can be null if the information was not extracted because of corrupt certificate data.

```csharp
public X509Certificate X509Certificate { get; }
```

#### Property Value

 [X509Certificate](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate)

### <a id="DotNetBrowser_Net_Certificates_Certificate_X509Certificate2"></a> X509Certificate2

The X509Certificate2 that provides access to all certificate information.
Can be null if the information was not extracted because of corrupt certificate data.

```csharp
public X509Certificate2 X509Certificate2 { get; }
```

#### Property Value

 [X509Certificate2](https://learn.microsoft.com/dotnet/api/system.security.cryptography.x509certificates.x509certificate2)

## Methods

### <a id="DotNetBrowser_Net_Certificates_Certificate_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

