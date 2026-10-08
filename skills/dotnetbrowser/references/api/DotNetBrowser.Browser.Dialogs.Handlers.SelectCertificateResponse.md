# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse"></a> Class SelectCertificateResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to <xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref>

```csharp
public sealed class SelectCertificateResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the SSL authorization should be
cancelled.

```csharp
public static SelectCertificateResponse Cancel()
```

#### Returns

 [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse_Select_DotNetBrowser_Net_Certificates_Certificate_"></a> Select\(Certificate\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the given certificate should be
selected.

```csharp
public static SelectCertificateResponse Select(Certificate certificate)
```

#### Parameters

`certificate` [Certificate](DotNetBrowser.Net.Certificates.Certificate.md)

The certificate that should be selected.

#### Returns

 [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse_Select_DotNetBrowser_Net_Certificates_Certificate_System_Byte___"></a> Select\(Certificate, byte\[\]\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the given certificate should be
selected.

```csharp
public static SelectCertificateResponse Select(Certificate certificate, byte[] privateKey)
```

#### Parameters

`certificate` [Certificate](DotNetBrowser.Net.Certificates.Certificate.md)

The certificate that should be selected.

`privateKey` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The private key for this certificate in PKCS#8 DER-encoded form.

#### Returns

 [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse_Select_System_Int32_"></a> Select\(int\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the client certificate from the
list with the given index should be selected.

```csharp
public static SelectCertificateResponse Select(int index)
```

#### Parameters

`index` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The index of the certificate that should be selected.

#### Returns

 [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref> implementation.

