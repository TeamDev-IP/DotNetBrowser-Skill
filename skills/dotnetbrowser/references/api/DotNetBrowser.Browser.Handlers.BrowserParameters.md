# <a id="DotNetBrowser_Browser_Handlers_BrowserParameters"></a> Class BrowserParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md)

#### Derived

[CreatePopupParameters](DotNetBrowser.Browser.Handlers.CreatePopupParameters.md), 
[FrameParameters](DotNetBrowser.Browser.Handlers.FrameParameters.md), 
[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md), 
[OpenPopupParameters](DotNetBrowser.Browser.Handlers.OpenPopupParameters.md), 
[PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md), 
[RequestPrintParameters](DotNetBrowser.Browser.Handlers.RequestPrintParameters.md), 
[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.SaveCreditCardParameters.md), 
[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.SavePasswordParameters.md), 
[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.SaveUserDataProfileParameters.md), 
[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.ShowContextMenuParameters.md), 
[StartDownloadParameters](DotNetBrowser.Downloads.Handlers.StartDownloadParameters.md), 
[StartPresentationParameters](DotNetBrowser.Cast.Handlers.StartPresentationParameters.md), 
[StartSessionParameters](DotNetBrowser.Capture.Handlers.StartSessionParameters.md), 
[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.md), 
[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Handlers_BrowserParameters_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

