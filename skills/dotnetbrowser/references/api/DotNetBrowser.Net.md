# <a id="DotNetBrowser_Net"></a> Namespace DotNetBrowser.Net

### Namespaces

 [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)

 [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)

 [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)

 [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)

### Classes

 [BytesData](DotNetBrowser.Net.md#DotNetBrowser_Net_BytesData)

The upload data as bytes.
Can be empty if the form doesn't contain any data.

 [FileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_FileValue)

 [FormData](DotNetBrowser.Net.md#DotNetBrowser_Net_FormData)

The list of key-value pairs each representing a segment of a form data.
Can be empty if the form doesn't contain any data.

 [HostPortPair](DotNetBrowser.Net.md#DotNetBrowser_Net_HostPortPair)

A host/port pair of the URI.

 [HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

The MIME type.

 [MultipartFormData](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormData)

The list of key-value pairs each representing a segment of a multi-part form data.
Can be empty if the form doesn't contain any data.

 [MultipartFormDataKeyValuePair](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormDataKeyValuePair)

A key-value pair that represents a segment of a multi-part form data. Can contain values
corresponding a form field content, an upload file content, etc.

 [Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

The scheme component of a URL.

 [TextData](DotNetBrowser.Net.md#DotNetBrowser_Net_TextData)

The upload data of the <code>text/plain</code> content type.

 [UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData)

The base class for all upload data.

 [UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

Represents the URL request received from the Chromium engine.

 [UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

The URL request job for the intercepted URL request, which allows you to provide the response data for
this URL request.

 [UrlRequestJobExtensions](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJobExtensions)

Provides extension methods for <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

### Interfaces

 [IFileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_IFileValue)

File data.

 [IHttpAuthPreferences](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpAuthPreferences)

The HTTP authorization preferences.

 [IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)

Represents the single HTTP header with all its values.

 [INetwork](DotNetBrowser.Net.md#DotNetBrowser_Net_INetwork)

Allows access and modifying to the network-level activities.

 [IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

 [IUploadData<T\>](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData_1)

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

### Enums

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)

The network errors.

 [RequestStatus](DotNetBrowser.Net.md#DotNetBrowser_Net_RequestStatus)

The status of a URL request.

 [SslVersion](DotNetBrowser.Net.md#DotNetBrowser_Net_SslVersion)

The supported SSL connection versions.

## <a id="DotNetBrowser_Net_BytesData"></a> Class BytesData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data as bytes.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class BytesData : UploadData, IUploadData<IReadOnlyList<byte>>, IUploadData
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData) ← 
[BytesData](DotNetBrowser.Net.md#DotNetBrowser_Net_BytesData)

##### Implements

[IUploadData<IReadOnlyList<byte\>\>](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData_1), 
[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_BytesData__ctor_System_Byte___"></a> BytesData\(byte\[\]\)

Creates a new instance containing the specified data.

```csharp
public BytesData(byte[] data)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The upload data as a byte array.

### Properties

#### <a id="DotNetBrowser_Net_BytesData_Data"></a> Data

The upload data as a read-only list.

```csharp
public IReadOnlyList<byte> Data { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[byte](https://learn.microsoft.com/dotnet/api/system.byte)\>

### Operators

#### <a id="DotNetBrowser_Net_BytesData_op_Implicit_System_Byte____DotNetBrowser_Net_BytesData"></a> implicit operator BytesData\(byte\[\]\)

Converts the specified data to a new instance of <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref>.

```csharp
public static implicit operator BytesData(byte[] data)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The upload data as a byte array.

##### Returns

 [BytesData](DotNetBrowser.Net.md#DotNetBrowser_Net_BytesData)

The new <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Net_FileValue"></a> Class FileValue

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class FileValue : IFileValue
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_FileValue)

##### Implements

[IFileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_IFileValue)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_FileValue__ctor_System_String_DotNetBrowser_Net_MimeType_System_String_"></a> FileValue\(string, MimeType, string\)

Constructor for FileValue.

```csharp
public FileValue(string fileName, MimeType contentType, string filePath)
```

##### Parameters

`fileName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file name. Cannot be empty.

`contentType` [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

A string representing the content type determined by the file extension. Equals
`application/octet-stream` when there's no MIME type associated with the file extension.

`filePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file path. Cannot be empty.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when file name or path is null or empty.

#### <a id="DotNetBrowser_Net_FileValue__ctor_System_String_DotNetBrowser_Net_MimeType_System_Byte___"></a> FileValue\(string, MimeType, byte\[\]\)

Constructor for FileValue.

```csharp
public FileValue(string fileName, MimeType contentType, byte[] bytes)
```

##### Parameters

`fileName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file name. Cannot be empty.

`contentType` [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

A string representing the content type determined by the file extension. Equals
`application/octet-stream` when there's no MIME type associated with the file extension.

`bytes` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The byte sequence representing the file upload data segment.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when file name is null or empty.
when bytes array is null.

### Properties

#### <a id="DotNetBrowser_Net_FileValue_Bytes"></a> Bytes

The file value as an array of bytes.

```csharp
public byte[] Bytes { get; }
```

##### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

#### <a id="DotNetBrowser_Net_FileValue_ContentType"></a> ContentType

The content type determined by the file extension. Equals
<code>application/octet-stream</code> when there is no MIME type associated with the file
extension.

```csharp
public MimeType ContentType { get; }
```

##### Property Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_FileValue_FileName"></a> FileName

The file name.

```csharp
public string FileName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_FileValue_FilePath"></a> FilePath

The file value as a file path.

```csharp
public string FilePath { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_FormData"></a> Class FormData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The list of key-value pairs each representing a segment of a form data.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class FormData : UploadData, IUploadData<IReadOnlyCollection<KeyValuePair<string, string>>>, IUploadData
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData) ← 
[FormData](DotNetBrowser.Net.md#DotNetBrowser_Net_FormData)

##### Implements

[IUploadData<IReadOnlyCollection<KeyValuePair<string, string\>\>\>](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData_1), 
[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_FormData__ctor_System_Collections_Generic_IReadOnlyCollection_System_Collections_Generic_KeyValuePair_System_String_System_String___"></a> FormData\(IReadOnlyCollection<KeyValuePair<string, string\>\>\)

Creates a new instance containing the specified key-value pairs.

```csharp
public FormData(IReadOnlyCollection<KeyValuePair<string, string>> data)
```

##### Parameters

`data` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[KeyValuePair](https://learn.microsoft.com/dotnet/api/system.collections.generic.keyvaluepair\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>\>

The key-value pairs that represent segments of the form data.

### Properties

#### <a id="DotNetBrowser_Net_FormData_Data"></a> Data

The key-value pairs that represent segments of the form data.

```csharp
public IReadOnlyCollection<KeyValuePair<string, string>> Data { get; }
```

##### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[KeyValuePair](https://learn.microsoft.com/dotnet/api/system.collections.generic.keyvaluepair\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>\>

## <a id="DotNetBrowser_Net_HostPortPair"></a> Class HostPortPair

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

A host/port pair of the URI.

```csharp
public sealed class HostPortPair
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HostPortPair](DotNetBrowser.Net.md#DotNetBrowser_Net_HostPortPair)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_HostPortPair_Host"></a> Host

Gets the host of the URI.

```csharp
public string Host { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_HostPortPair_Port"></a> Port

Gets the port of the URI.

```csharp
public int Port { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Net_HostPortPair_HasPort"></a> HasPort\(\)

Checks whether this host/port pair has a port.

```csharp
public bool HasPort()
```

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the port of this host/port pair is greater than null.

#### <a id="DotNetBrowser_Net_HostPortPair_Parse_System_String_"></a> Parse\(string\)

Converts a string representation of a host/port pair to the <xref href="DotNetBrowser.Net.HostPortPair" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static HostPortPair Parse(string hostPort)
```

##### Parameters

`hostPort` [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation of the host/port pair separated with the colon.

##### Returns

 [HostPortPair](DotNetBrowser.Net.md#DotNetBrowser_Net_HostPortPair)

the <xref href="DotNetBrowser.Net.HostPortPair" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Net_HostPortPair_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_HttpHeader"></a> Class HttpHeader

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class HttpHeader : IHttpHeader
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)

##### Implements

[IHttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpHeader)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_HttpHeader__ctor_System_String_System_String___"></a> HttpHeader\(string, params string\[\]\)

Creates the HTTP header instance using its name and values collection.

```csharp
public HttpHeader(string name, params string[] values)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTTP header name

`values` [string](https://learn.microsoft.com/dotnet/api/system.string)\[\]

The collection of the HTTP header values

### Properties

#### <a id="DotNetBrowser_Net_HttpHeader_Name"></a> Name

Gets the HTTP header name.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_HttpHeader_Values"></a> Values

Gets the collection of the HTTP header values.

```csharp
public IEnumerable<string> Values { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

## <a id="DotNetBrowser_Net_MimeType"></a> Class MimeType

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The MIME type.

```csharp
public sealed class MimeType : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Net_MimeType_ApplicationFormUrlEncoded"></a> ApplicationFormUrlEncoded

Gets the "application/x-www-form-urlencoded" MIME type.

```csharp
public static readonly MimeType ApplicationFormUrlEncoded
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ApplicationJson"></a> ApplicationJson

Gets the "application/json" MIME type.

```csharp
public static readonly MimeType ApplicationJson
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ApplicationOctetStream"></a> ApplicationOctetStream

Gets the "application/octet-stream" MIME type.

```csharp
public static readonly MimeType ApplicationOctetStream
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ApplicationPdf"></a> ApplicationPdf

Gets the "application/pdf" MIME type.

```csharp
public static readonly MimeType ApplicationPdf
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ApplicationXml"></a> ApplicationXml

Gets the "application/xml" MIME type.

```csharp
public static readonly MimeType ApplicationXml
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ApplicationZip"></a> ApplicationZip

Gets the "application/zip" MIME type.

```csharp
public static readonly MimeType ApplicationZip
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ImageGif"></a> ImageGif

Gets the "image/gif" MIME type.

```csharp
public static readonly MimeType ImageGif
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ImageJpeg"></a> ImageJpeg

Gets the "image/jpeg" MIME type.

```csharp
public static readonly MimeType ImageJpeg
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_ImagePng"></a> ImagePng

Gets the "image/png" MIME type.

```csharp
public static readonly MimeType ImagePng
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_MultipartFormData"></a> MultipartFormData

Gets the "multipart/form-data" MIME type.

```csharp
public static readonly MimeType MultipartFormData
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_TextCss"></a> TextCss

Gets the "text/css" MIME type.

```csharp
public static readonly MimeType TextCss
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_TextHtml"></a> TextHtml

Gets the "text/html" MIME type.

```csharp
public static readonly MimeType TextHtml
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_TextJavascript"></a> TextJavascript

Gets the "text/javascript" MIME type.

```csharp
public static readonly MimeType TextJavascript
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_MimeType_TextPlain"></a> TextPlain

Gets the "text/plain" MIME type.

```csharp
public static readonly MimeType TextPlain
```

##### Field Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

### Methods

#### <a id="DotNetBrowser_Net_MimeType_Create_System_String_"></a> Create\(string\)

Creates the MimeType instance from string representation.

```csharp
public static MimeType Create(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

##### Returns

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

the corresponding <xref href="DotNetBrowser.Net.MimeType" data-throw-if-not-resolved="false"></xref> instance.

### Operators

#### <a id="DotNetBrowser_Net_MimeType_op_Explicit_System_String__DotNetBrowser_Net_MimeType"></a> explicit operator MimeType\(string\)

Creates the MimeType instance from string representation.

```csharp
public static explicit operator MimeType(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

##### Returns

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

the corresponding <xref href="DotNetBrowser.Net.MimeType" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Net_MultipartFormData"></a> Class MultipartFormData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The list of key-value pairs each representing a segment of a multi-part form data.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class MultipartFormData : UploadData, IUploadData<IReadOnlyCollection<MultipartFormDataKeyValuePair>>, IUploadData
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData) ← 
[MultipartFormData](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormData)

##### Implements

[IUploadData<IReadOnlyCollection<MultipartFormDataKeyValuePair\>\>](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData_1), 
[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_MultipartFormData__ctor_System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Net_MultipartFormDataKeyValuePair__"></a> MultipartFormData\(IReadOnlyCollection<MultipartFormDataKeyValuePair\>\)

Creates a new instance containing the specified key-value pairs.

```csharp
public MultipartFormData(IReadOnlyCollection<MultipartFormDataKeyValuePair> data)
```

##### Parameters

`data` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[MultipartFormDataKeyValuePair](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormDataKeyValuePair)\>

The key-value pairs that represent segments of the multi-part form data.

### Properties

#### <a id="DotNetBrowser_Net_MultipartFormData_Data"></a> Data

The key-value pairs that represent segments of the multi-part form data.

```csharp
public IReadOnlyCollection<MultipartFormDataKeyValuePair> Data { get; }
```

##### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[MultipartFormDataKeyValuePair](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormDataKeyValuePair)\>

## <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair"></a> Class MultipartFormDataKeyValuePair

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

A key-value pair that represents a segment of a multi-part form data. Can contain values
corresponding a form field content, an upload file content, etc.

```csharp
public sealed class MultipartFormDataKeyValuePair
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MultipartFormDataKeyValuePair](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormDataKeyValuePair)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair__ctor_System_String_DotNetBrowser_Net_FileValue_"></a> MultipartFormDataKeyValuePair\(string, FileValue\)

Creates an instance from the given key and value.

```csharp
public MultipartFormDataKeyValuePair(string key, FileValue value)
```

##### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

The form content segment key.

`value` [FileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_FileValue)

The segment value representing the file content.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">key</code> is null or empty. /&gt; is null.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">value</code> is null.

#### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair__ctor_System_String_System_String_"></a> MultipartFormDataKeyValuePair\(string, string\)

Creates an instance from the given key and value.

```csharp
public MultipartFormDataKeyValuePair(string key, string value)
```

##### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

The form content segment key.

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The segment value representing the form content segment value. Can be empty if the
<code class="paramref">key</code>does not correspond to any value. For example, an empty
form field

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">key</code> is null or empty. /&gt; is null.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">value</code> is null.

### Properties

#### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_FileValue"></a> FileValue

The file representation of the data.

```csharp
public IFileValue FileValue { get; }
```

##### Property Value

 [IFileValue](DotNetBrowser.Net.md#DotNetBrowser_Net_IFileValue)

#### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_Key"></a> Key

The form content segment key.

```csharp
public string Key { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_StringValue"></a> StringValue

The string representation of the data.

```csharp
public string StringValue { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_Scheme"></a> Class Scheme

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The scheme component of a URL.

```csharp
public sealed class Scheme : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Net_Scheme_Http"></a> Http

The HTTP scheme.

```csharp
public static readonly Scheme Http
```

##### Field Value

 [Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

#### <a id="DotNetBrowser_Net_Scheme_Https"></a> Https

The HTTPS scheme.

```csharp
public static readonly Scheme Https
```

##### Field Value

 [Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

### Properties

#### <a id="DotNetBrowser_Net_Scheme_IsInterceptable"></a> IsInterceptable

Indicates whether this scheme is interceptable.

```csharp
public bool IsInterceptable { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### Methods

#### <a id="DotNetBrowser_Net_Scheme_Create_System_String_"></a> Create\(string\)

Creates the Scheme instance from string representation.

```csharp
public static Scheme Create(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

##### Returns

 [Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

the corresponding <xref href="DotNetBrowser.Net.Scheme" data-throw-if-not-resolved="false"></xref> instance.

### Operators

#### <a id="DotNetBrowser_Net_Scheme_op_Explicit_System_String__DotNetBrowser_Net_Scheme"></a> explicit operator Scheme\(string\)

Creates the Scheme instance from string representation.

```csharp
public static explicit operator Scheme(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

##### Returns

 [Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme)

the corresponding <xref href="DotNetBrowser.Net.Scheme" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Net_TextData"></a> Class TextData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data of the <code>text/plain</code> content type.

```csharp
public sealed class TextData : UploadData, IUploadData<string>, IUploadData
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData) ← 
[TextData](DotNetBrowser.Net.md#DotNetBrowser_Net_TextData)

##### Implements

[IUploadData<string\>](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData_1), 
[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Net_TextData__ctor_System_String_"></a> TextData\(string\)

Creates a new instance containing the specified data.

```csharp
public TextData(string data)
```

##### Parameters

`data` [string](https://learn.microsoft.com/dotnet/api/system.string)

The upload data as a <code>string</code>.

### Properties

#### <a id="DotNetBrowser_Net_TextData_Data"></a> Data

The upload data as a <code>string</code>.

```csharp
public string Data { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Operators

#### <a id="DotNetBrowser_Net_TextData_op_Implicit_System_String__DotNetBrowser_Net_TextData"></a> implicit operator TextData\(string\)

Converts the specified data to a new instance of <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref>.

```csharp
public static implicit operator TextData(string data)
```

##### Parameters

`data` [string](https://learn.microsoft.com/dotnet/api/system.string)

The upload data as a byte array.

##### Returns

 [TextData](DotNetBrowser.Net.md#DotNetBrowser_Net_TextData)

The new <xref href="DotNetBrowser.Net.TextData" data-throw-if-not-resolved="false"></xref>instance.

## <a id="DotNetBrowser_Net_UploadData"></a> Class UploadData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The base class for all upload data.

```csharp
public abstract class UploadData : IUploadData
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData)

##### Derived

[BytesData](DotNetBrowser.Net.md#DotNetBrowser_Net_BytesData), 
[FormData](DotNetBrowser.Net.md#DotNetBrowser_Net_FormData), 
[MultipartFormData](DotNetBrowser.Net.md#DotNetBrowser_Net_MultipartFormData), 
[TextData](DotNetBrowser.Net.md#DotNetBrowser_Net_TextData)

##### Implements

[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Net_UrlRequest"></a> Class UrlRequest

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Represents the URL request received from the Chromium engine.

```csharp
public sealed class UrlRequest
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_UrlRequest_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this request.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Net_UrlRequest_Method"></a> Method

Gets the HTTP method used to perform current request.

```csharp
public string Method { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_UrlRequest_ResourceType"></a> ResourceType

Gets the <xref href="DotNetBrowser.Net.Handlers.ResourceType" data-throw-if-not-resolved="false"></xref> of the resource the request is loading.

```csharp
public ResourceType ResourceType { get; }
```

##### Property Value

 [ResourceType](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ResourceType)

#### <a id="DotNetBrowser_Net_UrlRequest_SslVersion"></a> SslVersion

Gets the SSL connection version used to make this
request if it is available and the current request represents an HTTPS request.

```csharp
public SslVersion? SslVersion { get; }
```

##### Property Value

 [SslVersion](DotNetBrowser.Net.md#DotNetBrowser_Net_SslVersion)?

#### <a id="DotNetBrowser_Net_UrlRequest_TotalBytesReceived"></a> TotalBytesReceived

Gets the total amount of data received from network after SSL decoding and proxy
handling.

```csharp
public long TotalBytesReceived { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### <a id="DotNetBrowser_Net_UrlRequest_TotalBytesSent"></a> TotalBytesSent

Gets the total amount of data sent over the network before SSL encoding and proxy
handling.

```csharp
public long TotalBytesSent { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### <a id="DotNetBrowser_Net_UrlRequest_Url"></a> Url

Gets the requested URL address.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Net_UrlRequest_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_UrlRequest_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Net_UrlRequestJob"></a> Class UrlRequestJob

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The URL request job for the intercepted URL request, which allows you to provide the response data for
this URL request.

```csharp
public sealed class UrlRequestJob : IAutoDisposable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

##### Extension Methods

[UrlRequestJobExtensions.Write\(UrlRequestJob, Stream, int\)](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJobExtensions_Write_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Int32_), 
[UrlRequestJobExtensions.WriteAsync\(UrlRequestJob, Stream, CancellationToken, int\)](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJobExtensions_WriteAsync_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Threading_CancellationToken_System_Int32_)

### Properties

#### <a id="DotNetBrowser_Net_UrlRequestJob_IsClosed"></a> IsClosed

Indicates if the request is handled and all the data is sent.

```csharp
public bool IsClosed { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

The request is marked as handled when either <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> is called.

#### <a id="DotNetBrowser_Net_UrlRequestJob_IsDisposed"></a> IsDisposed

Indicates if the object is already disposed.

```csharp
public bool IsDisposed { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_UrlRequestJob_UrlRequest"></a> UrlRequest

Gets the <xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref> associated with this job.

```csharp
public UrlRequest UrlRequest { get; }
```

##### Property Value

 [UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

### Methods

#### <a id="DotNetBrowser_Net_UrlRequestJob_Complete"></a> Complete\(\)

Marks the request as completed. It can be used to indicate that all response data are already sent.

```csharp
public void Complete()
```

#### <a id="DotNetBrowser_Net_UrlRequestJob_Fail"></a> Fail\(\)

Marks the request as failed. It can be used to indicate that an error occurred during writing the
response data.

```csharp
public void Fail()
```

#### <a id="DotNetBrowser_Net_UrlRequestJob_Write_System_Byte___"></a> Write\(byte\[\]\)

Appends a chunk of the response data. This method may be called multiple
times to append several chunks.

```csharp
public void Write(byte[] data)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The response data bytes.

##### Remarks

When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
completed or failed.

#### <a id="DotNetBrowser_Net_UrlRequestJob_Write_System_Byte___System_Int32_System_Int32_"></a> Write\(byte\[\], int, int\)

Appends a segment of the response data. This method may be called multiple
times to append several chunks.

```csharp
public void Write(byte[] data, int offset, int count)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The buffer containing the response data bytes.

`offset` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The zero-based byte offset in <code class="paramref">data</code>.

`count` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of bytes to write.

##### Remarks

When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
completed or failed.

#### <a id="DotNetBrowser_Net_UrlRequestJob_WriteAsync_System_Byte___"></a> WriteAsync\(byte\[\]\)

Appends a chunk of the response data asynchronously. This method may be called multiple
times to append several chunks.

```csharp
public Task WriteAsync(byte[] data)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The response data bytes.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

##### Remarks

<p>
    Prefer this method over <xref href="DotNetBrowser.Net.UrlRequestJob.Write(System.Byte%5b%5d)" data-throw-if-not-resolved="false"></xref> when calling from an async context or a
    <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref>-based handler, as it does not block the
    calling thread while waiting for the data to be sent to the browser engine.
</p>
<p>
    When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
    or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
    completed or failed.
</p>

#### <a id="DotNetBrowser_Net_UrlRequestJob_WriteAsync_System_Byte___System_Int32_System_Int32_"></a> WriteAsync\(byte\[\], int, int\)

Appends a segment of the response data asynchronously. This method may be called multiple
times to append several chunks.

```csharp
public Task WriteAsync(byte[] data, int offset, int count)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The buffer containing the response data bytes.

`offset` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The zero-based byte offset in <code class="paramref">data</code>.

`count` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of bytes to write.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

##### Remarks

<p>
    Prefer this method over <xref href="DotNetBrowser.Net.UrlRequestJob.Write(System.Byte%5b%5d%2cSystem.Int32%2cSystem.Int32)" data-throw-if-not-resolved="false"></xref> when calling from an async context or a
    <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref>-based handler, as it does not block the
    calling thread while waiting for the data to be sent to the browser engine.
</p>
<p>
    When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
    or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
    completed or failed.
</p>

#### <a id="DotNetBrowser_Net_UrlRequestJob_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
public event EventHandler Disposed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler)

## <a id="DotNetBrowser_Net_UrlRequestJobExtensions"></a> Class UrlRequestJobExtensions

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Provides extension methods for <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

```csharp
public static class UrlRequestJobExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJobExtensions](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJobExtensions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Net_UrlRequestJobExtensions_Write_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Int32_"></a> Write\(UrlRequestJob, Stream, int\)

Reads all bytes from <code class="paramref">stream</code> and writes them to the URL request job.

```csharp
public static void Write(this UrlRequestJob job, Stream stream, int bufferSize = 81920)
```

##### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

The URL request job to write the data to.

`stream` [Stream](https://learn.microsoft.com/dotnet/api/system.io.stream)

The stream to read the data from.

`bufferSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The size of the buffer used to read the stream. Must be greater than zero.

##### Remarks

The stream is read in chunks to avoid buffering the entire content in memory.
After all data is written, call <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or
<xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> to finish the request.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">job</code> or <code class="paramref">stream</code> is <code>null</code>.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

<code class="paramref">bufferSize</code> is less than or equal to zero, or greater than <xref href="System.Int32.MaxValue" data-throw-if-not-resolved="false"></xref> - 56.

#### <a id="DotNetBrowser_Net_UrlRequestJobExtensions_WriteAsync_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Threading_CancellationToken_System_Int32_"></a> WriteAsync\(UrlRequestJob, Stream, CancellationToken, int\)

Reads all bytes from <code class="paramref">stream</code> and writes them to the URL request job asynchronously.

```csharp
public static Task WriteAsync(this UrlRequestJob job, Stream stream, CancellationToken cancellationToken = default, int bufferSize = 81920)
```

##### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

The URL request job to write the data to.

`stream` [Stream](https://learn.microsoft.com/dotnet/api/system.io.stream)

The stream to read the data from.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

The token to monitor for cancellation requests.

`bufferSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The size of the buffer used to read the stream. Must be greater than zero.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

##### Remarks

<p>
    The stream is read in chunks to avoid buffering the entire content in memory.
    The calling thread is released while waiting for each chunk to be sent to the
    browser engine, making this method suitable for use inside <code>Task.Run</code> or
    <code>async</code> handlers.
</p>
<p>
    After all data is written, call <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or
    <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> to finish the request.
</p>

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">job</code> or <code class="paramref">stream</code> is <code>null</code>.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

<code class="paramref">bufferSize</code> is less than or equal to zero, or greater than <xref href="System.Int32.MaxValue" data-throw-if-not-resolved="false"></xref> - 56.

## <a id="DotNetBrowser_Net_IFileValue"></a> Interface IFileValue

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

File data.

```csharp
public interface IFileValue
```

### Remarks

<p>
    Depending on how the request was constructed can contain the path to a file, or the
    bytes representing a file.
</p>
<p>
    For example, it contains the path when the value is taken from an
    <code> &lt;input type="file"&gt; </code>
    element of the submitted form.
</p>
<p>
    May contain bytes in case the request in the <code>multipart/form-data</code>
    format was constructed manually in a JavaScript code.
</p>

### Properties

#### <a id="DotNetBrowser_Net_IFileValue_Bytes"></a> Bytes

The file value as an array of bytes.

```csharp
byte[] Bytes { get; }
```

##### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

#### <a id="DotNetBrowser_Net_IFileValue_ContentType"></a> ContentType

The content type determined by the file extension. Equals
<code>application/octet-stream</code> when there is no MIME type associated with the file
extension.

```csharp
MimeType ContentType { get; }
```

##### Property Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Net_IFileValue_FileName"></a> FileName

The file name.

```csharp
string FileName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_IFileValue_FilePath"></a> FilePath

The file value as a file path.

```csharp
string FilePath { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Net_IHttpAuthPreferences"></a> Interface IHttpAuthPreferences

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The HTTP authorization preferences.

```csharp
public interface IHttpAuthPreferences
```

### Properties

#### <a id="DotNetBrowser_Net_IHttpAuthPreferences_DelegateWhiteList"></a> DelegateWhiteList

Gets or sets the HTTP network delegate authorization white list of URLs.
By default, network delegate white list is empty.

```csharp
string DelegateWhiteList { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.IHttpAuthPreferences" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_IHttpAuthPreferences_ServerWhiteList"></a> ServerWhiteList

Gets or sets the server HTTP authorization white list of URLs.
By default, server white list is empty.

```csharp
string ServerWhiteList { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.IHttpAuthPreferences" data-throw-if-not-resolved="false"></xref> object has already been disposed.

## <a id="DotNetBrowser_Net_IHttpHeader"></a> Interface IHttpHeader

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Represents the single HTTP header with all its values.

```csharp
public interface IHttpHeader
```

### Properties

#### <a id="DotNetBrowser_Net_IHttpHeader_Name"></a> Name

Gets the HTTP header name.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_IHttpHeader_Values"></a> Values

Gets the collection of the HTTP header values.

```csharp
IEnumerable<string> Values { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

## <a id="DotNetBrowser_Net_INetwork"></a> Interface INetwork

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Allows access and modifying to the network-level activities.

```csharp
public interface INetwork : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Net_INetwork_AcceptLanguage"></a> AcceptLanguage

Gets or sets the <code>Accept-Language</code> request header value.

```csharp
string AcceptLanguage { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Examples

<code>"fr, en-gb;q=0.8, en;q=0.7"</code> would mean: "I prefer French, but
will accept British English and other types of English."
Note, that all languages which are assigned a quality factor
greater than 0 are acceptable.

##### Remarks

This field restricts the set of natural languages that are preferred as a response to the request.
The default <code>Accept-Language</code> is <code>"en-us"</code>.
See <a href="https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html">https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html</a>
W3 Documentation.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The value is set to null or an empty string.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_AuthenticateHandler"></a> AuthenticateHandler

Gets or sets a handler that is used when the website requests authentication.

```csharp
IHandler<AuthenticateParameters, AuthenticateResponse> AuthenticateHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[AuthenticateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateParameters), [AuthenticateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_AuthenticateResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Continue(System.String%2cSystem.String)" data-throw-if-not-resolved="false"></xref> method
    to continue authentication process.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method
    to cancel authentication process.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.AuthenticateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_CanAccessFileHandler"></a> CanAccessFileHandler

Gets or sets a handler that is used when the Chromium engine is about to access the requested file. Can be used
to disallow accessing the file.

```csharp
IHandler<CanAccessFileParameters, CanAccessFileResponse> CanAccessFileHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[CanAccessFileParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileParameters), [CanAccessFileResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanAccessFileResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Can" data-throw-if-not-resolved="false"></xref> method
    to allow access to the file.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Cannot" data-throw-if-not-resolved="false"></xref> method
    to disallow access to the file.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse.Can" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_CanGetCookiesHandler"></a> CanGetCookiesHandler

Gets or sets a handler that is used when Chromium engine decides
whether cookies can be sent back to the web server.

```csharp
IHandler<CanGetCookiesParameters, CanGetCookiesResponse> CanGetCookiesHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[CanGetCookiesParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesParameters), [CanGetCookiesResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanGetCookiesResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Allow" data-throw-if-not-resolved="false"></xref> method to
    allow cookies to be sent to the web server.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Deny" data-throw-if-not-resolved="false"></xref> method to
    disallow cookies to be sent to the web server.
</p>
<p>
    If exception occurs inside the handler, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanGetCookiesResponse.Allow" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_CanSetCookieHandler"></a> CanSetCookieHandler

Gets or sets a handler that is used when Chromium engine decides
whether cookie can be saved for the URL or not.

```csharp
IHandler<CanSetCookieParameters, CanSetCookieResponse> CanSetCookieHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[CanSetCookieParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieParameters), [CanSetCookieResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_CanSetCookieResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Allow" data-throw-if-not-resolved="false"></xref> method to
    allow engine to save the cookie.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Deny" data-throw-if-not-resolved="false"></xref> method to
    deny engine to save the cookie. It will not be available
    via the <xref href="DotNetBrowser.Cookies.ICookieStore" data-throw-if-not-resolved="false"></xref> object.
</p>
<p>
    If exception occurs inside the handler, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.CanSetCookieResponse.Allow" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_HttpAuthPreferences"></a> HttpAuthPreferences

Gets the HTTP authorization preferences.

```csharp
IHttpAuthPreferences HttpAuthPreferences { get; }
```

##### Property Value

 [IHttpAuthPreferences](DotNetBrowser.Net.md#DotNetBrowser_Net_IHttpAuthPreferences)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Net_INetwork_ReceiveHeadersHandler"></a> ReceiveHeadersHandler

Gets or sets a handler that is used each time that an HTTP(S) response header is received. Due to redirects
and authentication requests this can happen multiple times per request. This event is intended
to allow adding, modifying, and deleting HTTP response headers, such as incoming "Set-Cookie" headers.

```csharp
IHandler<ReceiveHeadersParameters, ReceiveHeadersResponse> ReceiveHeadersHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersParameters), [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_ReceiveHeadersResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.OverrideHeaders(System.Collections.Generic.IEnumerable%7bDotNetBrowser.Net.HttpHeader%7d)" data-throw-if-not-resolved="false"></xref> method to override headers.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.Continue" data-throw-if-not-resolved="false"></xref> method to continue without modifications.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_SendUploadDataHandler"></a> SendUploadDataHandler

Gets or sets a handler that is used when the upload data is about to send to the web server.
Can be used to override the upload data before it is sent.

```csharp
IHandler<SendUploadDataParameters, SendUploadDataResponse> SendUploadDataHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SendUploadDataParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataParameters), [SendUploadDataResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUploadDataResponse)\>

##### Remarks

<p>
    Use one of the following methods to modify the upload data:

<ul>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.TextData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.FormData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.MultipartFormData)" data-throw-if-not-resolved="false"></xref>
        </li>
        <li>
            <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Override(DotNetBrowser.Net.BytesData)" data-throw-if-not-resolved="false"></xref>
        </li>
    </ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Continue" data-throw-if-not-resolved="false"></xref> method if you
    do not need to modify the upload data.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.SendUploadDataResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_SendUrlRequestHandler"></a> SendUrlRequestHandler

Gets or sets a handler that is used when an HTTP request is about to occur. It can be used to override the
requested URL and
redirect the request to another location.

```csharp
IHandler<SendUrlRequestParameters, SendUrlRequestResponse> SendUrlRequestHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SendUrlRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestParameters), [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_SendUrlRequestResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Override(System.String)" data-throw-if-not-resolved="false"></xref> method to
    override the requested URL.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Continue" data-throw-if-not-resolved="false"></xref> method to
    proceed without changes.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to
    cancel the request with the <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> error.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_StartTransactionHandler"></a> StartTransactionHandler

Gets or sets a handler that is used when the request is about to start the transaction process.
It allows adding, modifying, and deleting HTTP request headers.

```csharp
IHandler<StartTransactionParameters, StartTransactionResponse> StartTransactionHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[StartTransactionParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionParameters), [StartTransactionResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_StartTransactionResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.OverrideHeaders(System.Collections.Generic.IEnumerable%7bDotNetBrowser.Net.HttpHeader%7d)" data-throw-if-not-resolved="false"></xref> method
    to override headers.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.Continue" data-throw-if-not-resolved="false"></xref> method
    to continue with original headers.
</p>
<p>
    If exception occurs inside the handler, the default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse.Continue" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_UserAgent"></a> UserAgent

Gets the default user-agent string.

```csharp
string UserAgent { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    The default user-agent string can be configured through the
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.UserAgent" data-throw-if-not-resolved="false"></xref> property. If the default
    user-agent string has not been specified, then this method returns a string obtained from the
    Chromium engine.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_VerifyCertificateHandler"></a> VerifyCertificateHandler

Gets or sets a handler that is used to verify the SSL certificate provided by the web server.

```csharp
IHandler<VerifyCertificateParameters, VerifyCertificateResponse> VerifyCertificateHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[VerifyCertificateParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateParameters), [VerifyCertificateResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_VerifyCertificateResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Valid" data-throw-if-not-resolved="false"></xref> method if the SSL certificate
    should be accepted.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Invalid" data-throw-if-not-resolved="false"></xref> method if the SSL certificate
    must be rejected.
</p>
<p>
    Use the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Default" data-throw-if-not-resolved="false"></xref> method to let Chromium decide
    whether
    SSL certificate should be accepted or rejected.
</p>
<p>
    If this method throws an exception, then default behavior will be
    applied - the <xref href="DotNetBrowser.Net.Handlers.VerifyCertificateResponse.Default" data-throw-if-not-resolved="false"></xref> method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### Methods

#### <a id="DotNetBrowser_Net_INetwork_CreateUrlRequestJob_DotNetBrowser_Net_UrlRequest_DotNetBrowser_Net_Handlers_UrlRequestJobOptions_"></a> CreateUrlRequestJob\(UrlRequest, UrlRequestJobOptions\)

Creates a new <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref> instance with the given <code class="paramref">options</code>.

<p>The URL request job is used to provide the response data for the intercepted URL request.</p>

```csharp
UrlRequestJob CreateUrlRequestJob(UrlRequest request, UrlRequestJobOptions options = null)
```

##### Parameters

`request` [UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

The intercepted <xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref> instance to bind the job with.

`options` [UrlRequestJobOptions](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_UrlRequestJobOptions)

The options which are used to initialize the <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>

##### Returns

 [UrlRequestJob](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequestJob)

A new <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_ConnectionTypeChanged"></a> ConnectionTypeChanged

Occurs when the network connection type has been changed.

```csharp
event EventHandler<ConnectionTypeChangedEventArgs> ConnectionTypeChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ConnectionTypeChangedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs)\>

##### Remarks

<p>
    The event is raised whenever a change affects the route network packets
    take to any network server.
</p>
<p>
    For example, the event is triggered when:
</p>
<ul><li>A network connection becomes available or going away;</li><li>A VPN tunnel is established or taken down;</li><li>An active network connection's IP address changes.</li></ul>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_PacScriptErrorOccurred"></a> PacScriptErrorOccurred

Occurs when the error has been occured in the PAC script.

```csharp
event EventHandler<PacScriptErrorEventArgs> PacScriptErrorOccurred
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PacScriptErrorEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_PacScriptErrorEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_RedirectResponseCodeReceived"></a> RedirectResponseCodeReceived

Occurs when the redirect has been occured.

```csharp
event EventHandler<RedirectResponseCodeReceivedEventArgs> RedirectResponseCodeReceived
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_RequestCompleted"></a> RequestCompleted

Occurs when the request has been completed.

```csharp
event EventHandler<RequestCompletedEventArgs> RequestCompleted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RequestCompletedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestCompletedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_RequestDestroyed"></a> RequestDestroyed

Occurs when the request has been destroyed.

```csharp
event EventHandler<RequestDestroyedEventArgs> RequestDestroyed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RequestDestroyedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestDestroyedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_ResponseBytesReceived"></a> ResponseBytesReceived

Occurs when a part of HTTP response body has been received over the network.

```csharp
event EventHandler<ResponseBytesReceivedEventArgs> ResponseBytesReceived
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Net_INetwork_ResponseStarted"></a> ResponseStarted

Occurs when the response has been started.

```csharp
event EventHandler<ResponseStartedEventArgs> ResponseStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ResponseStartedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> object has already been disposed.

## <a id="DotNetBrowser_Net_IUploadData"></a> Interface IUploadData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

```csharp
public interface IUploadData
```

## <a id="DotNetBrowser_Net_IUploadData_1"></a> Interface IUploadData<T\>

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

```csharp
public interface IUploadData<out T> : IUploadData
```

##### Type Parameters

`T` 

The upload data type.

##### Implements

[IUploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_IUploadData)

### Properties

#### <a id="DotNetBrowser_Net_IUploadData_1_Data"></a> Data

Gets the upload data.

```csharp
T Data { get; }
```

##### Property Value

 T

## <a id="DotNetBrowser_Net_NetError"></a> Enum NetError

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The network errors.

```csharp
public enum NetError
```

### Fields

`Aborted = -3` 

An operation was aborted ( due to user action).



`AccessDenied = -10` 

Permission to access a resource, other than the network, was denied.



`AddUserCertFailed = -503` 

An error adding to the OS certificate database  = e.g. OS X Keychain,.



`AddressInUse = -147` 

Returned when attempting to bind an address that is already in use.



`AddressInvalid = -108` 

The IP address or port number is invalid  = e.g., cannot connect to the IP
address 0 or the port 0.



`AddressUnreachable = -109` 

The IP address is unreachable.  This usually means that there is no route
to the specified host or network.



`AlpnNegotiationFailed = -122` 

The request to negotiate an alternate protocol failed.



`BadSslClientAuthCert = -117` 

The SSL handshake failed because of a bad or missing client certificate.



`BlobDereferencedWhileBuilding = -904` 

The renderer destructed the blob before it was done transferring, and there were no outstanding references to
keep the blob alive.



`BlobFileWriteFailed = -902` 

A file could not be created or written.



`BlobInvalidConstructionArguments = -900` 

The construction arguments are invalid.



`BlobOutOfMemory = -901` 

There is not enough memory for the blob.



`BlobReferencedBlobBroken = -905` 

A blob referenced during construction is broken, or a browser-side builder tries to build a blob with a blob
reference that is not finished constructing.



`BlobReferencedFileUnavailable = -906` 

A file referenced during construction is not accessible to the renderer trying to create the blob.



`BlobSourceDiedInTransit = -903` 

The renderer was destroyed while data was in transit.



`BlockedByAdministrator = -22` 

The request was blocked by the URL blacklist configured by the domain administrator.



`BlockedByClient = -20` 

The client chose to block the request.



`BlockedByCsp = -30` 

The request was blocked by a Content Security Policy.



`BlockedByFingerprintingProtection = -34` 

The request was blocked by fingerprinting protections.



`BlockedByLocalNetworkAccessChecks = -385` 

The connection is blocked by private network access checks.



`BlockedByOrb = -32` 

The request was blocked by CORB or ORB.



`BlockedByResponse = -27` 

The request failed because the response was delivered along with requirements
which are not met ('X-Frame-Options' and 'Content-Security-Policy' ancestor
checks and 'Cross-Origin-Resource-Policy', for instance).



`BlockedInIncognitoByAdministrator = -35` 

The request was blocked by the Incognito Mode URL block list configured by the domain administrator.



`CacheAuthFailureAfterRead = -410` 

Received a challenge after the transaction has read some data, and the
credentials aren't available. There isn't a way to get them at that point.



`CacheChecksumMismatch = -408` 

The cache found an entry with an invalid checksum. This can be returned from
attempts to read from the cache. It is an internal error, returned by the
SimpleCache backend, but not by any URLRequest methods or members.



`CacheChecksumReadFailure = -407` 

The cache was unable to read a checksum record on an entry. This can be
returned from attempts to read from the cache. It is an internal error,
returned by the SimpleCache backend, but not by any URLRequest methods
or members.



`CacheCreateFailure = -405` 

The disk cache is unable to create this entry.



`CacheDoomFailure = -412` 

The disk cache is unable to doom this entry.



`CacheEntryNotSuitable = -411` 

Internal not-quite error code for the HTTP cache. In-memory hints suggest
that the cache entry would not have been useable with the transaction's
current configuration (e.g. load flags, mode, etc.).



`CacheLockTimeout = -409` 

Internal error code for the HTTP cache. The cache lock timeout has fired.



`CacheMiss = -400` 

The cache does not have the requested entry.



`CacheOpenFailure = -404` 

The disk cache is unable to open this entry.



`CacheOpenOrCreateFailure = -413` 

The disk cache is unable to open or create this entry.



`CacheOperationNotSupported = -403` 

The operation is not supported for this entry.



`CacheRace = -406` 

Multiple transactions are racing to create disk cache entries. This is an
internal error returned from the HttpCache to the HttpCacheTransaction that
tells the transaction to restart the entry-creation logic because the state
of the cache has changed.



`CacheReadFailure = -401` 

Unable to read from the disk cache.



`CacheWriteFailure = -402` 

Unable to write to the disk cache.



`CachedIpAddressSpaceBlockedByLocalNetworkAccessPolicy = -384` 

The IP address space of the cached remote endpoint is blocked by private network access check.



`CertAuthorityInvalid = -202` 

<p>
    The server responded with a certificate that is signed by an authority we don't trust.
    The could mean:
</p>
<p>
    1. An attacker has substituted the real certificate for a cert that
    contains his public key and is signed by his cousin.
</p>
<p>
    2. The server operator has a legitimate certificate from a CA we don't
    know about, but should trust.
</p>
<p>
    3. The server is presenting a self-signed certificate, providing no
    defense against active attackers  = but foiling passive attackers.
</p>



`CertCommonNameInvalid = -200` 

<p>
    The server responded with a certificate whose common name did not match the host name.
    This could mean:
</p>
<p>
    1. An attacker has redirected our traffic to his server and is presenting a certificate
    for which he knows the private key.
</p>
<p>
    2. The server is misconfigured and responding with the wrong cert.
</p>
<p>
    3. The user is on a wireless network and is being redirected to the network's login page.
</p>
<p>
    4. The OS has used a DNS search suffix and the server doesn't have a certificate for
    the abbreviated name in the address bar.
</p>



`CertContainsErrors = -203` 

<p>
    The server responded with a certificate that contains errors.
    This error is not recoverable.
</p>
<p>
    MSDN describes this error as follows:
    "The SSL certificate contains errors."
    NOTE: It's unclear how this differs from ERR_CERT_INVALID. For consistency,
    use that code instead of this one from now on.
</p>



`CertDatabaseChanged = -714` 

The certificate database changed in some way.



`CertDateInvalid = -201` 

<p>
    The server responded with a certificate that, by our clock, appears to
    either not yet be valid or to have expired.  This could mean:
</p>
<p>
    1. An attacker is presenting an old certificate for which he has managed
    to obtain the private key.
</p>
<p>
    2. The server is misconfigured and is not presenting a valid cert.
</p>
<p>
    3. Our clock is wrong.
</p>



`CertEnd = -220` 

The value immediately past the last certificate error code.



`CertInvalid = -207` 

<p>
    The server responded with a certificate that is invalid.
    This error is not recoverable.
</p>
<p>
    MSDN describes this error as follows:
    "The SSL certificate is invalid."
</p>



`CertKnownInterceptionBlocked = -217` 

Indicates that a certificate is blocked due to known interception or manipulation.

This value is typically returned when a certificate validation process detects that
    the certificate has been intercepted or altered by a known intermediary, such as a security appliance or
    malicious actor. Applications can use this status to identify and respond to potential security
    threats.

`CertNameConstraintViolation = -212` 

The certificate claimed DNS names that are in violation of name constraints.



`CertNoRevocationMechanism = -204` 

The certificate has no mechanism for determining if it is revoked.  In
effect, this certificate cannot be revoked.



`CertNonUniqueName = -210` 

The host name specified in the certificate is not unique.



`CertRevoked = -206` 

The server responded with a certificate has been revoked.
We have the capability to ignore this error, but it is probably not the
thing to do.



`CertSelfSignedLocalNetwork = -219` 

The certificate is self-signed and it is being used for either an RFC1918 IP literal URL, or a URL ending in
<code>.local</code>.



`CertTransparencyRequired = -214` 

Certificate Transparency was required for this connection, but the server
did not provide CT information that complied with the policy.



`CertUnableToCheckRevocation = -205` 

<p>
    Revocation information for the security certificate for this site is not
    available.  This could mean:
</p>
<p>
    1. An attacker has compromised the private key in the certificate and is
    blocking our attempt to find out that the cert was revoked.
</p>
<p>
    2. The certificate is unrevoked, but the revocation server is busy or
    unavailable.
</p>



`CertValidityTooLong = -213` 

The certificate's validity period is too long.



`CertVerifierChanged = -716` 

The certificate verifier configuration changed in some way.



`CertWeakKey = -211` 

The server responded with a certificate that contains a weak key  = e.g.
a too-small RSA key.



`CertWeakSignatureAlgorithm = -208` 

The server responded with a certificate that is signed using a weak
signature algorithm.



`ClientAuthCertTypeUnsupported = -151` 

Server request for client certificate did not contain any types we support.



`ConnectionAborted = -103` 

A connection timed out as a result of not receiving an ACK for data sent.
This can include a FIN packet that did not get ACK'd.



`ConnectionClosed = -100` 

A connection was closed (corresponding to a TCP FIN).



`ConnectionFailed = -104` 

A connection attempt failed.



`ConnectionRefused = -102` 

A connection attempt was refused.



`ConnectionReset = -101` 

A connection was reset  = corresponding to a TCP RST.



`ConnectionTimedOut = -118` 

A connection attempt timed out.



`ContentDecodingFailed = -330` 

Content decoding of the response body failed.



`ContentDecodingInitFailed = -371` 

Initializing content decoding failed.



`ContentLengthMismatch = -354` 

The HTTP response body transferred fewer bytes than were advertised by the
Content-Length header when the connection is closed.



`ContextShutDown = -26` 

The request failed because the URLRequestContext is shutting down, or has
been shut down.



`CtConsistencyProofParsingFailed = -171` 

Certificate Transparency: Failed to parse the received consistency proof.



`CtSthIncomplete = -169` 

Certificate Transparency: Received a signed tree head whose JSON parsing was
OK but was missing some of the fields.



`CtSthParsingFailed = -168` 

Certificate Transparency: Received a signed tree head that failed to parse.



`DictionaryLoadFailed = -387` 

The compression dictionary cannot be loaded.



`DisallowedUrlScheme = -301` 

The scheme of the URL is disallowed.



`DnsCacheInvalidationInProgress = -815` 

Returned when DNS cache invalidation is in progress. This is a transient error. Callers may want to retry later.



`DnsCacheMiss = -804` 

The entry was not found in cache, for cache-only lookups.



`DnsFormatError = -816` 

The DNS server responded with a format error response code.



`DnsMalformedResponse = -800` 

DNS resolver received a malformed response.



`DnsNameHttpsOnly = -809` 

DNS identified the request as disallowed for insecure connection (<code>http</code>/<code>ws</code>).
The error should be handled as if an HTTP redirect was received to redirect to <code>https</code> or <code>wss</code>.



`DnsNoMatchingSupportedAlpn = -811` 

The hostname resolution of an HTTPS record was expected to be resolved with ALPN values of supported
protocols, but did not.



`DnsNotImplemented = -818` 

The DNS server responded that the query type is not implemented.



`DnsOtherFailure = -820` 

The DNS server responded with an rcode indicating that the request failed, but there is no specific error code
for the rcode.



`DnsRefused = -819` 

The DNS server responded that the request was refused.



`DnsRequestCancelled = -810` 

All DNS requests associated with this job have been cancelled.



`DnsSearchEmpty = -805` 

Suffix search list rules prevent resolution of the given host name.



`DnsSecureProbeRecordInvalid = -814` 

When checking whether secure DNS can be used, the response returned for the requested probe record either had
no answer or was invalid.



`DnsSecureResolverHostnameResolutionFailed = -808` 

Failed to resolve the hostname of a DNS-over-HTTPS server.



`DnsServerFailure = -817` 

The DNS server responded with a server failure response code.



`DnsServerRequiresTcp = -801` 

DNS server requires TCP



`DnsSortError = -806` 

Failed to sort addresses according to RFC3484.



`DnsTimedOut = -803` 

DNS transaction timed out.



`EarlyDataRejected = -178` 

TLS 1.3 early data was rejected by the server. This will be received before
any data is returned from the socket. The request should be retried with
early data disabled.



`EchFallbackCertificateInvalid = -184` 

ECH was enabled, the server was unable to decrypt the encrypted <code>ClientHello</code>, and additionally did not
present a certificate valid for the public name.



`EchNotNegotiated = -183` 

ECH was enabled, but the server was unable to decrypt the encrypted <code>ClientHello</code>.



`EmptyResponse = -324` 

The server closed the connection without sending any data.



`EncodingDetectionFailed = -340` 

Detecting the encoding of the response failed.



`Failed = -2` 

A generic failure occurred.



`FileExists = -16` 

The file already exists.



`FileNoSpace = -18` 

Not enough room left on the disk.



`FileNotFound = -6` 

The file or directory cannot be found.



`FilePathTooLong = -17` 

The path or file name is too long.



`FileTooBig = -8` 

The file is too large.



`FileVirusInfected = -19` 

The file has a virus.



`HeadersTruncated = -357` 

The HTTP headers were truncated by an EOF.



`HostResolverQueueTooLarge = -119` 

There are too many pending DNS resolves, so a request in the queue was aborted.



`Http11Required = -365` 

HTTP_1_1_REQUIRED error code received on HTTP/2 session.



`Http2CompressionError = -363` 

Decoding or encoding of compressed HTTP/2 headers failed.



`Http2FlowControlError = -361` 

The peer violated HTTP/2 flow control.



`Http2FrameSizeError = -362` 

The peer sent an improperly sized HTTP/2 frame.



`Http2InadequateTransportSecurity = -360` 

Transport security is inadequate for the HTTP/2 version.



`Http2RstStreamNoErrorReceived = -372` 

Received HTTP/2 RST_STREAM frame with NO_ERROR error code. This error should
be handled internally by HTTP/2 code, and should not make it above the
SpdyStream layer.



`Http2StreamClosed = -376` 

Received an HTTP/2 frame on a closed stream.



`HttpResponseCodeFailure = -379` 

The server returned a non-2xx HTTP response code.
Note that this error is only used by certain APIs that interpret the HTTP
response itself. URLRequest for instance just passes most non-2xx
response back as success.



`IcannNameCollision = -166` 

Resolving a hostname to an IP address list included the IPv4 address
"127.0.53.53". This is a special IP address which ICANN has recommended to
indicate there was a name collision, and alert admins to a potential
problem.



`ImportCaCertFailed = -705` 

CA import failed due to some other error.



`ImportCaCertNotCa = -703` 

CA import failed - not a CA cert.



`ImportCertAlreadyExists = -704` 

Import failed - certificate already exists in database.
Note it's a little weird this is an error but reimporting a PKCS12 is ok
= no-op,.  That's how Mozilla does it, though.



`ImportServerCertFailed = -706` 

Server certificate import failed due to some internal error.



`IncompleteChunkedEncoding = -355` 

The HTTP response body is transferred with Chunked-Encoding, but the
terminating zero-length chunk was never sent when the connection is closed.



`IncompleteSpdyHeaders = -347` 

SPDY Headers have been received, but not all of them - status or version
headers are missing, so we're expecting additional frames to complete them.



`InconsistentIpAddressSpace = -383` 

The IP address space of the remote endpoint differed from the previous observed value during the same request.



`InsecureResponse = -501` 

The server's response was insecure  = e.g. there was a cert error,.



`InsufficientResources = -12` 

There were not enough resources to complete the operation.



`InternetDisconnected = -106` 

The Internet connection has been lost.



`InvalidArgument = -4` 

An argument to the function is incorrect.



`InvalidAuthCredentials = -338` 

Credentials could not be established during HTTP Authentication.



`InvalidChunkedEncoding = -321` 

Error in chunked transfer encoding.



`InvalidEchConfigList = -182` 

The <code>ECHConfigList</code> fetched over DNS cannot be parsed.



`InvalidHandle = -5` 

The handle or file descriptor is invalid.



`InvalidHttpResponse = -370` 

The server was expected to return an HTTP/1.x response, but did not. Rather
than treat it as HTTP/0.9, this error is returned.



`InvalidRedirect = -303` 

Attempting to load an URL resulted in a redirect to an invalid URL.



`InvalidResponse = -320` 

The server's response was invalid.



`InvalidSignedExchange = -504` 

An error occurred while handling a signed exchange.



`InvalidUrl = -300` 

The URL is invalid.



`InvalidWebBundle = -505` 

An error occurred while handling a Web Bundle source.



`IoPending = -1` 

An asynchronous IO operation is not yet complete.  This usually does not
indicate a fatal error.  Typically this error will be generated as a
notification to wait for some external notification that the IO operation
finally completed.



`KeyGenerationFailed = -710` 

Key generation failed.



`MalformedIdentity = -329` 

The identity used for authentication is invalid.



`MandatoryProxyConfigurationFailed = -131` 

A mandatory proxy configuration could not be used. Currently this means that
a mandatory PAC script could not be fetched, parsed or executed.



`MethodNotSupported = -322` 

The server did not support the request method.



`MisconfiguredAuthEnvironment = -343` 

The environment was not set up correctly for authentication  = for
example, no KDC could be found or the principal is unknown.



`MissingAuthCredentials = -341` 

= GSSAPI, No Kerberos credentials were available during HTTP Authentication.



`MsgTooBig = -142` 

The message was too large for the transport.
= for example a UDP message which exceeds size threshold,.



`NameNotResolved = -105` 

The host name could not be resolved.



`NameResolutionFailed = -137` 

An error occurred when trying to do a name resolution  = DNS,.



`NetworkAccessDenied = -138` 

Permission to access the network was denied. This is used to distinguish
errors that were most likely caused by a firewall from other access denied errors.
See also ERR_ACCESS_DENIED.



`NetworkAccessRevoked = -33` 

The request was blocked because it originated from a frame that has disabled network access.



`NetworkChanged = -21` 

The network changed.



`NetworkIoSuspended = -331` 

An operation could not be completed because all network IO
is suspended.



`NoBufferSpace = -176` 

No socket buffer space is available.



`NoPrivateKeyForCert = -502` 

The server responded to a &lt;keygen&gt; with a generated client cert that we
don't have the matching private key for.



`NoSupportedProxies = -336` 

There are no supported proxies in the provided list.



`NotImplemented = -11` 

The operation failed because of unimplemented functionality.



`Ok = 1` 

No error.



`OutOfMemory = -13` 

Memory allocation failed.



`PacNotInDhcp = -348` 

No PAC URL configuration could be retrieved from DHCP. This can indicate
either a failure to retrieve the DHCP configuration, or that there was no
PAC URL configured in DHCP.



`PacScriptFailed = -327` 

The evaluation of the PAC script failed.



`PacScriptTerminated = -367` 

The PAC script terminated fatally and must be reloaded.



`Pkcs12ImportBadPassword = -701` 

PKCS #12 import failed due to incorrect password.



`Pkcs12ImportFailed = -702` 

PKCS #12 import failed due to other error.



`Pkcs12ImportInvalidFile = -708` 

PKCS #12 import failed due to invalid/corrupt file.



`Pkcs12ImportInvalidMac = -707` 

PKCS #12 import failed due to invalid MAC.



`Pkcs12ImportUnsupported = -709` 

PKCS #12 import failed due to unsupported features.



`PreconnectMaxSocketLimit = -133` 

We've hit the max socket limit for the socket pool while preconnecting.
We don't bother trying to preconnect more sockets.



`PrivateKeyExportFailed = -712` 

Failure to export private key.



`ProxyAuthRequested = -127` 

The proxy requested authentication  = for tunnel establishment.



`ProxyAuthRequestedWithNoConnection = -364` 

Proxy Auth Requested without a valid Client Socket Handle.



`ProxyAuthUnsupported = -115` 

The proxy requested authentication  = for tunnel establishment, with an unsupported method.



`ProxyCertificateInvalid = -136` 

The certificate presented by the HTTPS Proxy was invalid.



`ProxyConnectionFailed = -130` 

Could not create a connection to the proxy server. An error occurred either
in resolving its name, or in connecting a socket to it. Note that this does
NOT include failures during the actual "CONNECT" method of an HTTP proxy.



`ProxyDelegateCanceledConnectRequest = -187` 

The proxy delegate cancelled the proxy connection request.



`ProxyDelegateCanceledConnectResponse = -188` 

The proxy delegate cancelled the proxy connection response.



`ProxyHttp11Required = -366` 

HTTP_1_1_REQUIRED error code received on HTTP/2 session to proxy.



`ProxyUnableToConnectToDestination = -186` 

An attempt to proxy a request failed because the proxy was not able to successfully connect to the destination.



`QuicCertRootNotKnown = -380` 

The certificate presented on a QUIC connection does not chain to a known root
and the origin connected to is not on a list of domains where unknown roots
are allowed.



`QuicGoawayRequestCanBeRetried = -381` 

A <code>GOAWAY</code> frame has been received indicating that the request has not been processed and is safe to retry.



`QuicHandshakeFailed = -358` 

The QUIC crypto handshake failed. This means that the server was unable
to read any requests sent, so they may be resent.



`QuicProtocolError = -356` 

There is a QUIC protocol error.



`ReadIfReadyNotImplemented = -174` 

Socket ReadIfReady support is not implemented. This error should not be user
visible, because the normal Read() method is used as a fallback.



`RequestRangeNotSatisfiable = -328` 

The response was 416  = Requested range not satisfiable, and the server cannot
satisfy the range requested.



`ResponseBodyTooBigToDrain = -345` 

The HTTP response was too big to drain.



`ResponseHeadersMultipleContentDisposition = -349` 

The HTTP response contained multiple Content-Disposition headers.



`ResponseHeadersMultipleContentLength = -346` 

The HTTP response contained multiple distinct Content-Length headers.



`ResponseHeadersMultipleLocation = -350` 

The HTTP response contained multiple Location headers.



`ResponseHeadersTooBig = -325` 

The headers section of the response is too large.



`SelfSignedCertGenerationFailed = -713` 

Self-signed certificate generation failed.



`SocketIsConnected = -23` 

The socket is already connected.



`SocketNotConnected = -15` 

The socket is not connected.



`SocketReceiveBufferSizeUnchangeable = -162` 

Failed to set the socket's receive buffer size as requested, despite success
return code from setsockopt.



`SocketSendBufferSizeUnchangeable = -163` 

Failed to set the socket's send buffer size as requested, despite success
return code from setsockopt.



`SocketSetReceiveBufferSizeError = -160` 

Failed to set the socket's receive buffer size as requested.



`SocketSetSendBufferSizeError = -161` 

Failed to set the socket's send buffer size as requested.



`SocksConnectionFailed = -120` 

Failed establishing a connection to the SOCKS proxy server for a target host.



`SocksConnectionHostUnreachable = -121` 

The SOCKS proxy server failed establishing connection to the target host
because that host is unreachable.



`SpdyPingFailed = -352` 

SPDY server didn't respond to the PING message.



`SpdyProtocolError = -337` 

There is a SPDY protocol error.



`SpdyServerRefusedStream = -351` 

SPDY server refused the stream. Client should retry. This should never be a
user-visible error.



`SslBadRecordMacAlert = -126` 

An SSL peer sent us a fatal bad_record_mac alert. This has been observed from servers with
buggy DEFLATE support.



`SslClientAuthCertBadFormat = -164` 

Failed to import a client certificate from the platform store into the SSL
library.



`SslClientAuthCertNeeded = -110` 

The server requested a client certificate for SSL client authentication.



`SslClientAuthCertNoPrivateKey = -135` 

The SSL client certificate has no private key.



`SslClientAuthNoCommonAlgorithms = -177` 

There were no common signature algorithms between our client certificate
private key and the server's preferences.



`SslClientAuthPrivateKeyAccessDenied = -134` 

The permission to use the SSL client certificate's private key was denied.



`SslClientAuthSignatureFailed = -141` 

<p>
    We were unable to sign the CertificateVerify data of an SSL client auth
    handshake with the client certificate's private key.
</p>
<p>
    Possible causes for this include the user implicitly or explicitly
    denying access to the private key, the private key may not be valid for
    signing, the key may be relying on a cached handle which is no longer
    valid, or the CSP won't allow arbitrary data to be signed.
</p>



`SslDecompressionFailureAlert = -125` 

An SSL peer sent us a fatal decompression_failure alert. This typically occurs when a peer
selects DEFLATE compression in the mistaken belief that it supports it.



`SslDecryptErrorAlert = -153` 

An SSL peer sent us a fatal decrypt_error alert. This typically occurs when
a peer could not correctly verify a signature (in CertificateVerify or
ServerKeyExchange) or validate a Finished message.



`SslKeyUsageIncompatible = -181` 

The server's certificate has a keyUsage extension incompatible with the
negotiated TLS key exchange method.



`SslNoRenegotiation = -123` 

The peer sent an SSL no_renegotiation alert message.



`SslObsoleteCipher = -172` 

The SSL server required an unsupported cipher suite that has since been
removed. This error will temporarily be signaled on a fallback for one or two
releases immediately following a cipher suite's removal, after which the
fallback will be removed.



`SslPinnedKeyNotInCertChain = -150` 

The certificate didn't match the built-in public key pins for the host name.
The pins are set in net/http/transport_security_state.cc and require that one
of a set of public keys exist on the path from the leaf to the root.



`SslProtocolError = -107` 

An SSL protocol error occurred.



`SslRenegotiationRequested = -114` 

The server requested a renegotiation  = rehandshake,.



`SslServerCertBadFormat = -167` 

The SSL server presented a certificate which could not be decoded. This is
not a certificate error code as no X509Certificate object is available. This
error is fatal.



`SslServerCertChanged = -156` 

The SSL server certificate changed in a renegotiation.



`SslUnrecognizedNameAlert = -159` 

The SSL server sent us a fatal unrecognized_name alert.



`SslVersionOrCipherMismatch = -113` 

The client and server don't support a common SSL protocol version or cipher suite.



`TemporarilyThrottled = -139` 

The request throttler module cancelled this request to avoid DDOS.



`TimedOut = -7` 

An operation timed out.



`Tls13DowngradeDetected = -180` 

TLS 1.3 was enabled, but a lower version was negotiated and the server
returned a value indicating it supported TLS 1.3. This is part of a security
check in TLS 1.3, but it may also indicate the user is behind a buggy
TLS-terminating proxy which implemented TLS 1.2 incorrectly. (See
https://crbug.com/boringssl/226.)



`TooManyAcceptChRestarts = -382` 

The <code>ACCEPT_CH</code> restart has been triggered too many times.



`TooManyRedirects = -310` 

Attempting to load an URL resulted in too many redirects.



`TooManyRetries = -375` 

An HTTP transaction was retried too many times due for authentication or
invalid certificates. This may be due to a bug in the net stack that would
otherwise infinite loop, or if the server or proxy continually requests fresh
credentials or presents a fresh invalid certificate.



`TrustTokenOperationFailed = -506` 

A Trust Tokens protocol operation-executing request failed for one of a
number of reasons (precondition failure, internal error, bad response).



`TrustTokenOperationSuccessWithoutSendingRequest = -507` 

When handling a Trust Tokens protocol operation-executing request, the system
was able to execute the request's Trust Tokens operation without sending the
request to its destination: for instance, the results could have been present
in a local cache (for redemption) or the operation could have been diverted
to a local provider (for "platform-provided" issuance).



`TunnelConnectionFailed = -111` 

A tunnel connection through the proxy could not be established.



`UnableToReuseConnectionForProxyAuth = -170` 

The attempt to reuse a connection to send proxy auth credentials failed
before the AuthController was used to generate credentials. The caller should
reuse the controller with a new connection. This error is only used
internally by the network stack.



`UndocumentedSecurityLibraryStatus = -344` 

An undocumented SSPI or GSSAPI status code was returned.



`Unexpected = -9` 

An unexpected error.  This may be caused by a programming mistake or an invalid assumption.



`UnexpectedContentDictionaryHeader = -388` 

The header of a dictionary-compressed stream does not match the expected value.



`UnexpectedProxyAuth = -323` 

The response was 407  = Proxy Authentication Required,, yet we did not send
the request to a proxy.



`UnexpectedSecurityLibraryStatus = -342` 

An unexpected, but documented, SSPI or GSSAPI status code was returned.



`Unknown = 2` 

The error is unknown.



`UnknownUrlScheme = -302` 

The scheme of the URL is unknown.



`UnsafePort = -312` 

Attempting to load an URL with an unsafe port number.  These are port
numbers that correspond to services, which are not robust to spurious input
that may be constructed as a result of an allowed web construct  = e.g., HTTP
looks a lot like SMTP, so form submission to port 25 is denied,.



`UnsafeRedirect = -311` 

Attempting to load an URL resulted in an unsafe redirect  = e.g., a redirect
to file:// is considered unsafe.



`UnsupportedAuthScheme = -339` 

An HTTP Authentication scheme was tried which is not supported on this
machine.



`UploadFileChanged = -14` 

The file upload failed because the file's modification time was different from the expectation.



`UploadStreamRewindNotSupported = -25` 

The upload failed because the upload stream needed to be re-read, due to a
retry or a redirect, but the upload stream doesn't support that operation.



`WinsockUnexpectedWrittenBytes = -124` 

Winsock sometimes reports more data written than passed.  This is probably due to a broken LSP.



`WrongVersionOnEarlyData = -179` 

TLS 1.3 early data was offered, but the server responded with TLS 1.2 or
earlier. This is an internal error code to account for a
backwards-compatibility issue with early data and TLS 1.2. It will be
received before any data is returned from the socket. The request should be
retried with early data disabled.
See https://tools.ietf.org/html/rfc8446#appendix-D.3 for details.



`WsProtocolError = -145` 

Websocket protocol error. Indicates that we are terminating the connection
due to a malformed frame or other protocol violation.



`WsThrottleQueueTooLarge = -154` 

There are too many pending WebSocketJob instances, so the new job was not
pushed to the queue.



`WsUpgrade = -173` 

When a WebSocket handshake is done successfully and the connection has been
upgraded, the URLRequest is cancelled with this error code.



`ZstdWindowSizeTooBig = -386` 

Content decoding failed due to the zstd window size being too big (over 8 MB).

## <a id="DotNetBrowser_Net_RequestStatus"></a> Enum RequestStatus

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The status of a URL request.

```csharp
public enum RequestStatus
```

### Fields

`Canceled = 4` 

A request was cancelled programmatically.



`Failed = 5` 

A request failed for some reason.



`IoPending = 3` 

An IO request is pending. It is expected that the request issuer will be informed when it
is completed.



`Success = 2` 

A request succeeded.



`Unknown = 1` 

The request status is unknown.

## <a id="DotNetBrowser_Net_SslVersion"></a> Enum SslVersion

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The supported SSL connection versions.

```csharp
public enum SslVersion
```

### Fields

`Quic = 8` 

QUIC



`Ssl2 = 2` 

SSL 2.0



`Ssl3 = 3` 

SSL 3.0



`Tls1 = 4` 

TLS 1.0



`Tls11 = 5` 

TLS 1.1



`Tls12 = 6` 

TLS 1.2



`Tls13 = 7` 

TLS 1.3



`Unknown = 1` 

The SSL version cannot be determined.
