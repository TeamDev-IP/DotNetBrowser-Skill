# <a id="DotNetBrowser_Media_IAudio"></a> Interface IAudio

Namespace: [DotNetBrowser.Media](DotNetBrowser.Media.md)  
Assembly: DotNetBrowser.dll  

Allows controlling audio on the loaded web page and receive notifications when audio has been
started or stopped playing.

```csharp
public interface IAudio : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Media_IAudio_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Media_IAudio_IsPlaying"></a> IsPlaying

Indicates if the audio is currently playing on the loaded web page.

```csharp
bool IsPlaying { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Media_IAudio_Muted"></a> Muted

Mutes or unmutes all audio output for this Browser instance.

```csharp
bool Muted { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Media_IAudio_AudioPlaybackStarted"></a> AudioPlaybackStarted

Occurs when an audio has been started playing on the web page.

```csharp
event EventHandler<AudioPlaybackStartedEventArgs> AudioPlaybackStarted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioPlaybackStartedEventArgs](DotNetBrowser.Media.Events.AudioPlaybackStartedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Media_IAudio_AudioPlaybackStopped"></a> AudioPlaybackStopped

Occurs when an audio has been stopped playing on the web page.

```csharp
event EventHandler<AudioPlaybackStoppedEventArgs> AudioPlaybackStopped
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[AudioPlaybackStoppedEventArgs](DotNetBrowser.Media.Events.AudioPlaybackStoppedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> has already been disposed.

