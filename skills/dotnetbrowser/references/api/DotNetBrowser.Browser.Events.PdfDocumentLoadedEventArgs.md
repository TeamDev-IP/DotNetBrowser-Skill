# <a id="DotNetBrowser_Browser_Events_PdfDocumentLoadedEventArgs"></a> Class PdfDocumentLoadedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Browser.IBrowser.PdfDocumentLoaded" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class PdfDocumentLoadedEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[PdfDocumentLoadedEventArgs](DotNetBrowser.Browser.Events.PdfDocumentLoadedEventArgs.md)

#### Inherited Members

[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.BrowserEventArgs.md\#DotNetBrowser\_Browser\_Events\_BrowserEventArgs\_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Events_PdfDocumentLoadedEventArgs_Frame"></a> Frame

Gets the frame in which the PDF document has been loaded.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Browser_Events_PdfDocumentLoadedEventArgs_Url"></a> Url

Gets the URL of the PDF document.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

