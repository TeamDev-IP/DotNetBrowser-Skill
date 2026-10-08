# <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse"></a> Class SendUploadDataResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response for the <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUploadDataResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_UploadData"></a> UploadData

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

## Methods

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that uses the original upload data.

```csharp
public static SendUploadDataResponse Continue()
```

#### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_BytesData_"></a> Override\(BytesData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(BytesData uploadData)
```

#### Parameters

`uploadData` [BytesData](DotNetBrowser.Net.BytesData.md)

ByteData used for overriding

#### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_TextData_"></a> Override\(TextData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(TextData uploadData)
```

#### Parameters

`uploadData` [TextData](DotNetBrowser.Net.TextData.md)

TextData used for overriding

#### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_FormData_"></a> Override\(FormData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(FormData uploadData)
```

#### Parameters

`uploadData` [FormData](DotNetBrowser.Net.FormData.md)

FormData used for overriding

#### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUploadDataResponse_Override_DotNetBrowser_Net_MultipartFormData_"></a> Override\(MultipartFormData\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> that overrides the upload data.

```csharp
public static SendUploadDataResponse Override(MultipartFormData uploadData)
```

#### Parameters

`uploadData` [MultipartFormData](DotNetBrowser.Net.MultipartFormData.md)

MultipartFormData used for overriding

#### Returns

 [SendUploadDataResponse](DotNetBrowser.Net.Handlers.SendUploadDataResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUploadDataHandler" data-throw-if-not-resolved="false"></xref> implementation.

