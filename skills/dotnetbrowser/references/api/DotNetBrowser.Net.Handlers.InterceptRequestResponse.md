# <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse"></a> Class InterceptRequestResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the scheme handler.

```csharp
public sealed class InterceptRequestResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InterceptRequestResponse](DotNetBrowser.Net.Handlers.InterceptRequestResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse_Intercept_DotNetBrowser_Net_UrlRequestJob_"></a> Intercept\(UrlRequestJob\)

Creates a <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance indicating that
the request should be intercepted.

```csharp
public static InterceptRequestResponse Intercept(UrlRequestJob job)
```

#### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse.UrlRequestJob" data-throw-if-not-resolved="false"></xref> providing data of the HTTP response
that can be created using the <xref href="DotNetBrowser.Net.INetwork.CreateUrlRequestJob(DotNetBrowser.Net.UrlRequest%2cDotNetBrowser.Net.Handlers.UrlRequestJobOptions)" data-throw-if-not-resolved="false"></xref> method.

#### Returns

 [InterceptRequestResponse](DotNetBrowser.Net.Handlers.InterceptRequestResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in handler implementation.

### <a id="DotNetBrowser_Net_Handlers_InterceptRequestResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance indicating that
the request should be handled by the Chromium engine.

```csharp
public static InterceptRequestResponse Proceed()
```

#### Returns

 [InterceptRequestResponse](DotNetBrowser.Net.Handlers.InterceptRequestResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.InterceptRequestResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in the scheme handler implementation.

