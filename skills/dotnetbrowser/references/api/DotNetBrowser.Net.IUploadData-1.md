# <a id="DotNetBrowser_Net_IUploadData_1"></a> Interface IUploadData<T\>

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

#### Type Parameters

`T` 

The upload data type.

#### Implements

[IUploadData](DotNetBrowser.Net.IUploadData.md)

## Properties

### <a id="DotNetBrowser_Net_IUploadData_1_Data"></a> Data

Gets the upload data.

```csharp
T Data { get; }
```

#### Property Value

 T

