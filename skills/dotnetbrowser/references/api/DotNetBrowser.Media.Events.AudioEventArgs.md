# <a id="DotNetBrowser_Media_Events_AudioEventArgs"></a> Class AudioEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> related events.

```csharp
public class AudioEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.AudioEventArgs.md)

#### Derived

[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.AudioPlaybackStartedEventArgs.md), 
[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.AudioPlaybackStoppedEventArgs.md)

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

### <a id="DotNetBrowser_Media_Events_AudioEventArgs_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance that initiated this event.

```csharp
public IAudio Audio { get; }
```

#### Property Value

 [IAudio](DotNetBrowser.Media.IAudio.md)

