# <a id="DotNetBrowser_Browser_Events_BrowserEventArgs"></a> Class BrowserEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> events.

```csharp
public class BrowserEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md)

#### Derived

[AudioEventArgs](DotNetBrowser.Media.Events.AudioEventArgs.md), 
[BrowserBecameResponsiveEventArgs](DotNetBrowser.Browser.Events.BrowserBecameResponsiveEventArgs.md), 
[BrowserBecameUnresponsiveEventArgs](DotNetBrowser.Browser.Events.BrowserBecameUnresponsiveEventArgs.md), 
[CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.CastSessionStartFailedEventArgs.md), 
[ConsoleMessageReceivedEventArgs](DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.md), 
[FaviconChangedEventArgs](DotNetBrowser.Browser.Events.FaviconChangedEventArgs.md), 
[FocusGainedEventArgs](DotNetBrowser.Browser.Events.FocusGainedEventArgs.md), 
[FocusLostEventArgs](DotNetBrowser.Browser.Events.FocusLostEventArgs.md), 
[FocusRequestedEventArgs](DotNetBrowser.Browser.Events.FocusRequestedEventArgs.md), 
[FrameEventArgs](DotNetBrowser.Browser.Events.FrameEventArgs.md), 
[FullScreenEnteredEventArgs](DotNetBrowser.Browser.FullScreen.Events.FullScreenEnteredEventArgs.md), 
[FullScreenExitedEventArgs](DotNetBrowser.Browser.FullScreen.Events.FullScreenExitedEventArgs.md), 
[MediaStreamEventArgs](DotNetBrowser.Browser.Events.MediaStreamEventArgs.md), 
[PdfDocumentLoadFailedEventArgs](DotNetBrowser.Browser.Events.PdfDocumentLoadFailedEventArgs.md), 
[PdfDocumentLoadedEventArgs](DotNetBrowser.Browser.Events.PdfDocumentLoadedEventArgs.md), 
[PrintPreviewClosedEventArgs](DotNetBrowser.Browser.Events.PrintPreviewClosedEventArgs.md), 
[PrintPreviewOpenedEventArgs](DotNetBrowser.Browser.Events.PrintPreviewOpenedEventArgs.md), 
[RenderProcessTerminatedEventArgs](DotNetBrowser.Browser.Events.RenderProcessTerminatedEventArgs.md), 
[SessionStartedEventArgs](DotNetBrowser.Browser.Events.SessionStartedEventArgs.md), 
[StatusChangedEventArgs](DotNetBrowser.Browser.Events.StatusChangedEventArgs.md), 
[TitleChangedEventArgs](DotNetBrowser.Browser.Events.TitleChangedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Events_BrowserEventArgs_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

