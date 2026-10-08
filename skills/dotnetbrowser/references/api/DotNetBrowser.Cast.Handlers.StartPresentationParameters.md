# <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters"></a> Class StartPresentationParameters

Namespace: [DotNetBrowser.Cast.Handlers](DotNetBrowser.Cast.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Cast.ICast.StartPresentationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartPresentationParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[StartPresentationParameters](DotNetBrowser.Cast.Handlers.StartPresentationParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_AvailableReceivers"></a> AvailableReceivers

Gets the service that allows observing available media receivers.

```csharp
public IMediaReceivers AvailableReceivers { get; }
```

#### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.IMediaReceivers.md)

### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_PresentationRequest"></a> PresentationRequest

       Gets the JavaScript 

       <pre><code class="lang-csharp">PresentationRequest</code></pre>

initiated this presentation.

```csharp
public PresentationRequest PresentationRequest { get; }
```

#### Property Value

 [PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md)

### <a id="DotNetBrowser_Cast_Handlers_StartPresentationParameters_SupportedReceivers"></a> SupportedReceivers

Gets the list of media receivers that are able to start presentation from
<xref href="DotNetBrowser.Cast.Handlers.StartPresentationParameters.PresentationRequest" data-throw-if-not-resolved="false"></xref>.

```csharp
public IReadOnlyList<IMediaReceiver> SupportedReceivers { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

