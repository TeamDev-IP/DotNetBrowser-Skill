# <a id="DotNetBrowser_Cast_ICastSessions"></a> Interface ICastSessions

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that allows observing <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> cast
<xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> sessions.

```csharp
public interface ICastSessions
```

## Properties

### <a id="DotNetBrowser_Cast_ICastSessions_AllAlive"></a> AllAlive

Gets the list of <xref href="DotNetBrowser.Cast.ICastSession.IsAlive" data-throw-if-not-resolved="false"></xref> alive cast sessions.

```csharp
IReadOnlyList<ICastSession> AllAlive { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ICastSession](DotNetBrowser.Cast.ICastSession.md)\>

### <a id="DotNetBrowser_Cast_ICastSessions_Discovered"></a> Discovered

Occurs when a new <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been discovered in
the environment.

```csharp
event EventHandler<CastSessionDiscoveredEventArgs> Discovered
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionDiscoveredEventArgs](DotNetBrowser.Cast.Events.CastSessionDiscoveredEventArgs.md)\>

### <a id="DotNetBrowser_Cast_ICastSessions_StartFailed"></a> StartFailed

Occurs when a start of a <xref href="DotNetBrowser.Cast.ICastSession" data-throw-if-not-resolved="false"></xref> session has been failed.

```csharp
event EventHandler<CastSessionStartFailedEventArgs> StartFailed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.CastSessionStartFailedEventArgs.md)\>

