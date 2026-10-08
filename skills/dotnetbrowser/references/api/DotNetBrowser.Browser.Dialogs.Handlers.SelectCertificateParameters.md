# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateParameters"></a> Class SelectCertificateParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.SelectCertificateHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SelectCertificateParameters : CommonDialogParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[CommonDialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md) ← 
[SelectCertificateParameters](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.md)

#### Inherited Members

[CommonDialogParameters.Message](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_CommonDialogParameters\_Message), 
[CommonDialogParameters.Title](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_CommonDialogParameters\_Title), 
[DialogParameters.Browser](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_DialogParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateParameters_Certificates"></a> Certificates

Gets a collection of the certificates allowed by the server.

```csharp
public IEnumerable<Certificate> Certificates { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[Certificate](DotNetBrowser.Net.Certificates.Certificate.md)\>

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateParameters_RequestIssuedByProxy"></a> RequestIssuedByProxy

Indicates whether the request that requires the certificate selection is
issued by an HTTPS proxy server.

```csharp
public bool RequestIssuedByProxy { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateParameters_SslOrigin"></a> SslOrigin

Gets the host and port of the server that requested the client authentication.

```csharp
public HostPortPair SslOrigin { get; }
```

#### Property Value

 [HostPortPair](DotNetBrowser.Net.HostPortPair.md)

