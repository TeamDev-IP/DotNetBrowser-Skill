# <a id="DotNetBrowser_Net_Handlers_SendUploadDataParameters"></a> Class SendUploadDataParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUploadDataParameters : UrlRequestParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md) ← 
[SendUploadDataParameters](DotNetBrowser.Net.Handlers.SendUploadDataParameters.md)

#### Inherited Members

[UrlRequestParameters.UrlRequest](DotNetBrowser.Net.Handlers.UrlRequestParameters.md\#DotNetBrowser\_Net\_Handlers\_UrlRequestParameters\_UrlRequest), 
[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataParameters_UploadData"></a> UploadData

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header.If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

```csharp
public IUploadData UploadData { get; }
```

#### Property Value

 [IUploadData](DotNetBrowser.Net.IUploadData.md)

