# <a id="DotNetBrowser_Net_UrlRequest"></a> Class UrlRequest

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Represents the URL request received from the Chromium engine.

```csharp
public sealed class UrlRequest
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequest](DotNetBrowser.Net.UrlRequest.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_UrlRequest_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this request.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Net_UrlRequest_Method"></a> Method

Gets the HTTP method used to perform current request.

```csharp
public string Method { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_UrlRequest_ResourceType"></a> ResourceType

Gets the <xref href="DotNetBrowser.Net.Handlers.ResourceType" data-throw-if-not-resolved="false"></xref> of the resource the request is loading.

```csharp
public ResourceType ResourceType { get; }
```

#### Property Value

 [ResourceType](DotNetBrowser.Net.Handlers.ResourceType.md)

### <a id="DotNetBrowser_Net_UrlRequest_SslVersion"></a> SslVersion

Gets the SSL connection version used to make this
request if it is available and the current request represents an HTTPS request.

```csharp
public SslVersion? SslVersion { get; }
```

#### Property Value

 [SslVersion](DotNetBrowser.Net.SslVersion.md)?

### <a id="DotNetBrowser_Net_UrlRequest_TotalBytesReceived"></a> TotalBytesReceived

Gets the total amount of data received from network after SSL decoding and proxy
handling.

```csharp
public long TotalBytesReceived { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

### <a id="DotNetBrowser_Net_UrlRequest_TotalBytesSent"></a> TotalBytesSent

Gets the total amount of data sent over the network before SSL encoding and proxy
handling.

```csharp
public long TotalBytesSent { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

### <a id="DotNetBrowser_Net_UrlRequest_Url"></a> Url

Gets the requested URL address.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Net_UrlRequest_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_UrlRequest_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

