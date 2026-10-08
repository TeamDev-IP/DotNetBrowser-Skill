# <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs"></a> Class CastSessionDiscoveredEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> event.

<p>
    The new cast session is discovered after the user started casting media content via DotNetBrowser
    API, or another application, i.e.Google Chrome.
</p>

```csharp
public sealed class CastSessionDiscoveredEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[CastSessionDiscoveredEventArgs](DotNetBrowser.Cast.Events.CastSessionDiscoveredEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs_CastSession"></a> CastSession

Gets the discovered session.

```csharp
public ICastSession CastSession { get; }
```

#### Property Value

 [ICastSession](DotNetBrowser.Cast.ICastSession.md)

### <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs_CastSessions"></a> CastSessions

Gets the <xref href="DotNetBrowser.Cast.ICastSessions" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public ICastSessions CastSessions { get; }
```

#### Property Value

 [ICastSessions](DotNetBrowser.Cast.ICastSessions.md)

