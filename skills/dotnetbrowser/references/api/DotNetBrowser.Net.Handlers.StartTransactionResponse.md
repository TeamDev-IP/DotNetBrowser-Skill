# <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse"></a> Class StartTransactionResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartTransactionResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartTransactionResponse](DotNetBrowser.Net.Handlers.StartTransactionResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_HttpHeaders"></a> HttpHeaders

Gets the collection of the of HTTP headers with all its values.

```csharp
public IEnumerable<IHttpHeader> HttpHeaders { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IHttpHeader](DotNetBrowser.Net.IHttpHeader.md)\>

## Methods

### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> that starts the transaction
with the original headers.

```csharp
public static StartTransactionResponse Continue()
```

#### Returns

 [StartTransactionResponse](DotNetBrowser.Net.Handlers.StartTransactionResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_StartTransactionResponse_OverrideHeaders_System_Collections_Generic_IEnumerable_DotNetBrowser_Net_HttpHeader__"></a> OverrideHeaders\(IEnumerable<HttpHeader\>\)

Creates a <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> that overrides
headers and starts the transaction

```csharp
public static StartTransactionResponse OverrideHeaders(IEnumerable<HttpHeader> httpHeaders)
```

#### Parameters

`httpHeaders` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.HttpHeader.md)\>

HttpHeaders used for overriding

#### Returns

 [StartTransactionResponse](DotNetBrowser.Net.Handlers.StartTransactionResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.StartTransactionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.StartTransactionHandler" data-throw-if-not-resolved="false"></xref> implementation.

