# <a id="DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs"></a> Class CastSessionStoppedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSession.Stopped" data-throw-if-not-resolved="false"></xref> event.

<p>
    Also, the cast session is stopped when the user starts a new cast session to the
    <xref href="DotNetBrowser.Cast.ICastSession.MediaReceiver" data-throw-if-not-resolved="false"></xref> receiver of this cast session.
</p>

```csharp
public sealed class CastSessionStoppedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[CastSessionStoppedEventArgs](DotNetBrowser.Cast.Events.CastSessionStoppedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs_CastSession"></a> CastSession

Gets the cast session that has been stopped.

```csharp
public ICastSession CastSession { get; }
```

#### Property Value

 [ICastSession](DotNetBrowser.Cast.ICastSession.md)

