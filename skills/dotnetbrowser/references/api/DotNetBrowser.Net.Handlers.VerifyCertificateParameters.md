# <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters"></a> Class VerifyCertificateParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.VerifyCertificateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class VerifyCertificateParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.VerifyCertificateParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_Certificate"></a> Certificate

Gets the SSL certificate to verify.

```csharp
public Certificate Certificate { get; }
```

#### Property Value

 [Certificate](DotNetBrowser.Net.Certificates.Certificate.md)

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_HostName"></a> HostName

Gets the SSL server host name.

```csharp
public string HostName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_VerifyCertificateParameters_VerifyErrors"></a> VerifyErrors

Gets the verification errors that indicate result
of SSL certificate verification by the Chromium engine.
If this collection is empty, then default SSL certificate verifier couldn't find any issues with the
given certificate, so it's a valid certificate.

```csharp
public IEnumerable<CertificateVerificationError> VerifyErrors { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[CertificateVerificationError](DotNetBrowser.Net.Certificates.CertificateVerificationError.md)\>

