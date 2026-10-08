# <a id="DotNetBrowser_Browser_Events_FrameEventArgs"></a> Class FrameEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> events related to <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public class FrameEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[FrameEventArgs](DotNetBrowser.Browser.Events.FrameEventArgs.md)

#### Derived

[FrameCreatedEventArgs](DotNetBrowser.Browser.Events.FrameCreatedEventArgs.md), 
[FrameDeletedEventArgs](DotNetBrowser.Browser.Events.FrameDeletedEventArgs.md), 
[SpellCheckCompletedEventArgs](DotNetBrowser.Browser.Events.SpellCheckCompletedEventArgs.md)

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

### <a id="DotNetBrowser_Browser_Events_FrameEventArgs_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

