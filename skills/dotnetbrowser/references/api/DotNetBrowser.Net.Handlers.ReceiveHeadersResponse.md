# <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse"></a> Class ReceiveHeadersResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response for the <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ReceiveHeadersResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_HttpHeaders"></a> HttpHeaders

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> HttpHeaders { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)\>

## Methods

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> that uses headers without modification.

```csharp
public static ReceiveHeadersResponse Continue()
```

#### Returns

 [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_ReceiveHeadersResponse_OverrideHeaders_System_Collections_Generic_IEnumerable_DotNetBrowser_Net_HttpHeader__"></a> OverrideHeaders\(IEnumerable<HttpHeader\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> that overrides the received headers.

```csharp
public static ReceiveHeadersResponse OverrideHeaders(IEnumerable<HttpHeader> httpHeaders)
```

#### Parameters

`httpHeaders` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.HttpHeader.md)\>

HttpHeaders used for overriding

#### Returns

 [ReceiveHeadersResponse](DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.ReceiveHeadersResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.ReceiveHeadersHandler" data-throw-if-not-resolved="false"></xref> implementation.

