# <a id="DotNetBrowser_Browser_Events_MediaStreamEventArgs"></a> Class MediaStreamEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> events related to media stream events.

```csharp
public class MediaStreamEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[MediaStreamEventArgs](DotNetBrowser.Browser.Events.MediaStreamEventArgs.md)

#### Derived

[MediaStreamCaptureStartedEventArgs](DotNetBrowser.Browser.Events.MediaStreamCaptureStartedEventArgs.md), 
[MediaStreamCaptureStoppedEventArgs](DotNetBrowser.Browser.Events.MediaStreamCaptureStoppedEventArgs.md)

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

### <a id="DotNetBrowser_Browser_Events_MediaStreamEventArgs_MediaStreamType"></a> MediaStreamType

Gets the media type of the captured stream.

```csharp
public MediaStreamType MediaStreamType { get; }
```

#### Property Value

 [MediaStreamType](DotNetBrowser.Browser.Events.MediaStreamType.md)

