# <a id="DotNetBrowser_Cast_ICastSession"></a> Interface ICastSession

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A session of casting media content to a media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver.

<p>
    The session is <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> discovered when the user starts casting
    the browser/screen content or a presentation of media content via the DotNetBrowser API, or another
    application, i.e.Google Chrome. To indicate that the cast session has been started by another
    profile and, accordingly, a Chromium instance the <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> property is provided.
</p>

```csharp
public interface ICastSession
```

## Properties

### <a id="DotNetBrowser_Cast_ICastSession_Description"></a> Description

Gets the description of the session. Examples: "Mirroring tab (www.example.com)",
"Casting media", "Casting YouTube".

```csharp
string Description { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

The description may be empty when the session just started and Chromium didn't define the
cast content yet.

### <a id="DotNetBrowser_Cast_ICastSession_IsAlive"></a> IsAlive

Indicates whether this cast session is alive.

```csharp
bool IsAlive { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cast_ICastSession_IsLocal"></a> IsLocal

Indicates whether this cast session is initiated and managed by the current
<xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref>.

```csharp
bool IsLocal { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Cast_ICastSession_MediaReceiver"></a> MediaReceiver

Gets the media receiver of this session.

```csharp
IMediaReceiver MediaReceiver { get; }
```

#### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

#### Remarks

<p>
    The method may block the current thread if the receiver is not discovered yet. It may
    happen when the cast session is not <xref href="DotNetBrowser.Cast.ICastSession.IsLocal" data-throw-if-not-resolved="false"></xref> local and started on the
    receiver not yet discovered by the current instance of Chromium.
</p>

### <a id="DotNetBrowser_Cast_ICastSession_Mode"></a> Mode

Gets the mode of the session.

```csharp
CastMode Mode { get; }
```

#### Property Value

 [CastMode](DotNetBrowser.Cast.CastMode.md)

## Methods

### <a id="DotNetBrowser_Cast_ICastSession_Stop"></a> Stop\(\)

Stops the cast session.

```csharp
void Stop()
```

#### Remarks

<p>
    This method has no effect when this cast session is already stopped.
</p>

### <a id="DotNetBrowser_Cast_ICastSession_Stopped"></a> Stopped

Occurs when a <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been stopped.

<p>
    Also, the cast session is stopped when the user starts a new cast session to the
    <xref href="DotNetBrowser.Cast.ICastSession.MediaReceiver" data-throw-if-not-resolved="false"></xref> receiver of this cast session.
</p>

```csharp
event EventHandler<CastSessionStoppedEventArgs> Stopped
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionStoppedEventArgs](DotNetBrowser.Cast.Events.CastSessionStoppedEventArgs.md)\>

