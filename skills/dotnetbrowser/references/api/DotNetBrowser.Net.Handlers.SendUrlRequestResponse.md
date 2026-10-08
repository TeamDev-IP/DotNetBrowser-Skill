# <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse"></a> Class SendUrlRequestResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response of the <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SendUrlRequestResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SendUrlRequestResponse](DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_UrlToRequest"></a> UrlToRequest

Gets the new URL to request.

```csharp
public string UrlToRequest { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
cancels loading process with the <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> code.

```csharp
public static SendUrlRequestResponse Cancel()
```

#### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Continue"></a> Continue\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
continues loading process with the requested URL.

```csharp
public static SendUrlRequestResponse Continue()
```

#### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_SendUrlRequestResponse_Override_System_String_"></a> Override\(string\)

Creates a <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> that
overrides the requested URL.

```csharp
public static SendUrlRequestResponse Override(string url)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

New URL used for override

#### Returns

 [SendUrlRequestResponse](DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.SendUrlRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.SendUrlRequestHandler" data-throw-if-not-resolved="false"></xref> implementation.

