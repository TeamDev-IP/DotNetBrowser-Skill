# <a id="DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs"></a> Class ConnectionTypeChangedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ConnectionTypeChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ConnectionTypeChangedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ConnectionTypeChangedEventArgs](DotNetBrowser.Net.Events.ConnectionTypeChangedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs_ConnectionType"></a> ConnectionType

Gets the connection type of the network at the time of the event.

```csharp
public ConnectionType ConnectionType { get; }
```

#### Property Value

 [ConnectionType](DotNetBrowser.Net.Events.ConnectionType.md)

