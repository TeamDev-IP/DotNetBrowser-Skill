# <a id="DotNetBrowser_Cast_PresentationRequest"></a> Class PresentationRequest

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The JavaScript 

<pre><code class="lang-csharp">PresentationRequest</code></pre>

.

```csharp
public sealed class PresentationRequest : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_PresentationRequest_Frame"></a> Frame

Gets the frame from which the presentation has been requested.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Cast_PresentationRequest_OriginUrl"></a> OriginUrl

Gets the origin URL of the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> where the presentation
has been requested.

```csharp
public string OriginUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cast_PresentationRequest_PresentationUrls"></a> PresentationUrls

Gets all of URLs whose content will be cast.

```csharp
public IReadOnlyList<string> PresentationUrls { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

