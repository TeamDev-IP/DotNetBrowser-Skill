# <a id="DotNetBrowser_Browser_Handlers_FrameParameters"></a> Class FrameParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

Represents the parameters of <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref>-related handlers associated with <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public class FrameParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.FrameParameters.md)

#### Derived

[ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.ConvertJsNameParameters.md), 
[InjectCssParameters](DotNetBrowser.Browser.Handlers.InjectCssParameters.md), 
[InjectJsParameters](DotNetBrowser.Browser.Handlers.InjectJsParameters.md), 
[RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Handlers_FrameParameters_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

