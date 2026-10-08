# <a id="DotNetBrowser_Net"></a> Namespace DotNetBrowser.Net

### Namespaces

 [DotNetBrowser.Net.Certificates](DotNetBrowser.Net.Certificates.md)

 [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)

 [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)

 [DotNetBrowser.Net.Proxy](DotNetBrowser.Net.Proxy.md)

### Classes

 [BytesData](DotNetBrowser.Net.BytesData.md)

The upload data as bytes.
Can be empty if the form doesn't contain any data.

 [FileValue](DotNetBrowser.Net.FileValue.md)

 [FormData](DotNetBrowser.Net.FormData.md)

The list of key-value pairs each representing a segment of a form data.
Can be empty if the form doesn't contain any data.

 [HostPortPair](DotNetBrowser.Net.HostPortPair.md)

A host/port pair of the URI.

 [HttpHeader](DotNetBrowser.Net.HttpHeader.md)

 [MimeType](DotNetBrowser.Net.MimeType.md)

The MIME type.

 [MultipartFormData](DotNetBrowser.Net.MultipartFormData.md)

The list of key-value pairs each representing a segment of a multi-part form data.
Can be empty if the form doesn't contain any data.

 [MultipartFormDataKeyValuePair](DotNetBrowser.Net.MultipartFormDataKeyValuePair.md)

A key-value pair that represents a segment of a multi-part form data. Can contain values
corresponding a form field content, an upload file content, etc.

 [Scheme](DotNetBrowser.Net.Scheme.md)

The scheme component of a URL.

 [TextData](DotNetBrowser.Net.TextData.md)

The upload data of the <code>text/plain</code> content type.

 [UploadData](DotNetBrowser.Net.UploadData.md)

The base class for all upload data.

 [UrlRequest](DotNetBrowser.Net.UrlRequest.md)

Represents the URL request received from the Chromium engine.

 [UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

The URL request job for the intercepted URL request, which allows you to provide the response data for
this URL request.

 [UrlRequestJobExtensions](DotNetBrowser.Net.UrlRequestJobExtensions.md)

Provides extension methods for <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

### Interfaces

 [IFileValue](DotNetBrowser.Net.IFileValue.md)

File data.

 [IHttpAuthPreferences](DotNetBrowser.Net.IHttpAuthPreferences.md)

The HTTP authorization preferences.

 [IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)

Represents the single HTTP header with all its values.

 [INetwork](DotNetBrowser.Net.INetwork.md)

Allows access and modifying to the network-level activities.

 [IUploadData](DotNetBrowser.Net.IUploadData.md)

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

 [IUploadData<T\>](DotNetBrowser.Net.IUploadData\-1.md)

The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`,
`application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the
content of the `Content-Type` header. If the `Content-Type` header is missing or doesn't include
a valid substring indicating the corresponding upload data type, the upload data will be in a binary
format.

### Enums

 [NetError](DotNetBrowser.Net.NetError.md)

The network errors.

 [RequestStatus](DotNetBrowser.Net.RequestStatus.md)

The status of a URL request.

 [SslVersion](DotNetBrowser.Net.SslVersion.md)

The supported SSL connection versions.

