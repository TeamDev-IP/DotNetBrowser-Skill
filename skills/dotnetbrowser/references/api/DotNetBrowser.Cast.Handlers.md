# <a id="DotNetBrowser_Cast_Handlers"></a> Namespace DotNetBrowser.Cast.Handlers

### Classes

 [StartPresentationParameters](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationParameters)

The parameters of the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

 [StartPresentationResponse](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationResponse)

A response to the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters"></a> Class StartPresentationParameters

Namespace: [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartPresentationParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[StartPresentationParameters](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_AvailableReceivers"></a> AvailableReceivers

Gets the service that allows observing available media receivers.

```csharp
public IMediaReceivers AvailableReceivers { get; }
```

##### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceivers)

#### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_PresentationRequest"></a> PresentationRequest

       Gets the JavaScript 

       <pre><code class="lang-csharp">PresentationRequest</code></pre>

initiated this presentation.

```csharp
public PresentationRequest PresentationRequest { get; }
```

##### Property Value

 [PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest)

#### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_SupportedReceivers"></a> SupportedReceivers

Gets the list of media receivers that are able to start presentation from
<xref href="DotNetBrowser.Cast.Handlers.StartPresentationParameters.PresentationRequest" data-throw-if-not-resolved="false"></xref>.

```csharp
public IReadOnlyList<IMediaReceiver> SupportedReceivers { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)\>

## <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse"></a> Class StartPresentationResponse

Namespace: [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartPresentationResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartPresentationResponse](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the presentation
should be canceled.

```csharp
public static StartPresentationResponse Cancel()
```

##### Returns

 [StartPresentationResponse](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationResponse)

The <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Cast_Handlers_StartPresentationResponse_Start_DotNetBrowser_Cast_IMediaReceiver_"></a> Start\(IMediaReceiver\)

Creates a <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the presentation
should be started on the <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

```csharp
public static StartPresentationResponse Start(IMediaReceiver mediaReceiver)
```

##### Parameters

`mediaReceiver` [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

##### Returns

 [StartPresentationResponse](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationResponse)

The <xref href="DotNetBrowser.Cast.Handlers.StartPresentationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref> implementation.
