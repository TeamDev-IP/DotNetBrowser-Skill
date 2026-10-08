# <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse"></a> Class VerifyCertificateResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>

```csharp
public sealed class VerifyCertificateResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Default"></a> Default\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that lets Chromium decide
whether SSL certificate should be accepted or rejected.

```csharp
public static VerifyCertificateResponse Default()
```

#### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Invalid"></a> Invalid\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine
that the given certificate is invalid with the <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus.Invalid" data-throw-if-not-resolved="false"></xref>.

```csharp
public static VerifyCertificateResponse Invalid()
```

#### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Invalid_System_Collections_Generic_IList_DotNetBrowser_Net_Certificates_CertificateVerificationStatus__"></a> Invalid\(IList<CertificateVerificationStatus\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine
that the given certificate is invalid with the specific <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus" data-throw-if-not-resolved="false"></xref>.

```csharp
public static VerifyCertificateResponse Invalid(IList<CertificateVerificationStatus> certificateVerificationStatuses)
```

#### Parameters

`certificateVerificationStatuses` [IList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ilist\-1)<[CertificateVerificationStatus](DotNetBrowser.Net.Certificates.CertificateVerificationStatus.md)\>

The list of statuses that explain why the certificate is invalid.

#### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

<p>
    If the status list is null or empty the <xref href="DotNetBrowser.Net.Certificates.CertificateVerificationStatus.Invalid" data-throw-if-not-resolved="false"></xref> value will
    be used.
</p>

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateResponse_Valid"></a> Valid\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> that marks SSL certificate
as valid and must be accepted.

```csharp
public static VerifyCertificateResponse Valid()
```

#### Returns

 [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

