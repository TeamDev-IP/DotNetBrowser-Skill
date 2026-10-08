# <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse"></a> Class StartPresentationResponse

Namespace: [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartPresentationResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartPresentationResponse](DotNetBrowser.Cast.Handlers.StartPresentationResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the presentation
should be canceled.

```csharp
public static StartPresentationResponse Cancel()
```

#### Returns

 [StartPresentationResponse](DotNetBrowser.Cast.Handlers.StartPresentationResponse.md)

The <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse_Start_DotNetBrowser_Cast_IMediaReceiver_"></a> Start\(IMediaReceiver\)

Creates a <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the presentation
should be started on the <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

```csharp
public static StartPresentationResponse Start(IMediaReceiver mediaReceiver)
```

#### Parameters

`mediaReceiver` [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

#### Returns

 [StartPresentationResponse](DotNetBrowser.Cast.Handlers.StartPresentationResponse.md)

The <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref> implementation.

