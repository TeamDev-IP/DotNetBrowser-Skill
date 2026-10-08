# <a id="DotNetBrowser_Capture_Events_SessionStoppedEventArgs"></a> Class SessionStoppedEventArgs

Namespace: [DotNetBrowser.Capture.Events](DotNetBrowser.Capture.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Capture.ISession.Stopped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class SessionStoppedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[SessionStoppedEventArgs](DotNetBrowser.Capture.Events.SessionStoppedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Capture_Events_SessionStoppedEventArgs_Session"></a> Session

Gets the <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> instance that has been stopped.

```csharp
public ISession Session { get; }
```

#### Property Value

 [ISession](DotNetBrowser.Capture.ISession.md)

