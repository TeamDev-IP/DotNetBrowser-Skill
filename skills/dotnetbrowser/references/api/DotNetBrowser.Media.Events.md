# <a id="DotNetBrowser_Media_Events"></a> Namespace DotNetBrowser.Media.Events

### Classes

 [AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs)

The base class for <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> related events.

 [AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStarted" data-throw-if-not-resolved="false"></xref> event.

 [AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStopped" data-throw-if-not-resolved="false"></xref> event.

## <a id="DotNetBrowser_Media_Events_AudioEventArgs"></a> Class AudioEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> related events.

```csharp
public class AudioEventArgs : BrowserEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs)

##### Derived

[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs), 
[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

##### Inherited Members

[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Media_Events_AudioEventArgs_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance that initiated this event.

```csharp
public IAudio Audio { get; }
```

##### Property Value

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

## <a id="DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs"></a> Class AudioPlaybackStartedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioPlaybackStartedEventArgs : AudioEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs) ← 
[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStartedEventArgs)

##### Inherited Members

[AudioEventArgs.Audio](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs_Audio), 
[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs"></a> Class AudioPlaybackStoppedEventArgs

Namespace: [DotNetBrowser.Media.Events](DotNetBrowser.Media.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Media.IAudio.AudioPlaybackStopped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class AudioPlaybackStoppedEventArgs : AudioEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[AudioEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs) ← 
[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioPlaybackStoppedEventArgs)

##### Inherited Members

[AudioEventArgs.Audio](DotNetBrowser.Media.Events.md#DotNetBrowser_Media_Events_AudioEventArgs_Audio), 
[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)
