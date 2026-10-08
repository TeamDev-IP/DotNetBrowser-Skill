# <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters"></a> Class ReceiveHeadersParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ReceiveHeadersParameters : UrlRequestParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[UrlRequestParameters](DotNetBrowser.Net.Handlers.UrlRequestParameters.md) ← 
[ReceiveHeadersParameters](DotNetBrowser.Net.Handlers.ReceiveHeadersParameters.md)

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

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_Charset"></a> Charset

Gets the charset in lower case from the headers. If there's no charset,
returns empty string.

```csharp
public string Charset { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_ContentLength"></a> ContentLength

Gets the number of the content length.

```csharp
public long ContentLength { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_Headers"></a> Headers

Gets the collection of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> Headers { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)\>

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_MimeType"></a> MimeType

Gets the MIME type in lower case from the headers. If there's no MIME
type, returns empty string.

```csharp
public MimeType MimeType { get; }
```

#### Property Value

 [MimeType](DotNetBrowser.Net.MimeType.md)

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_StatusLine"></a> StatusLine

Gets the first line of a Response message which is the StatusLine,
consisting of the protocol version followed by a numeric status code
and its associated textual phrase.

```csharp
public string StatusLine { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersParameters_StatusText"></a> StatusText

Gets the status text.

```csharp
public string StatusText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

