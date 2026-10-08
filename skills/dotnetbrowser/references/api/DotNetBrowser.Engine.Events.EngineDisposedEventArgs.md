# <a id="DotNetBrowser_Engine_Events_EngineDisposedEventArgs"></a> Class EngineDisposedEventArgs

Namespace: [DotNetBrowser.Engine.Events](DotNetBrowser.Engine.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the event indicating that the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has been disposed.

```csharp
public class EngineDisposedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[EngineDisposedEventArgs](DotNetBrowser.Engine.Events.EngineDisposedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Engine_Events_EngineDisposedEventArgs_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance that has been disposed.

```csharp
public IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Engine_Events_EngineDisposedEventArgs_ExitCode"></a> ExitCode

Gets the exit code of the main Chromium process that has been terminated.

```csharp
public long ExitCode { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

