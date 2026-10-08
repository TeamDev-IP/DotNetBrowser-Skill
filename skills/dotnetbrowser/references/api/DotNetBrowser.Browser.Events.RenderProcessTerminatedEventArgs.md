# <a id="DotNetBrowser_Browser_Events_RenderProcessTerminatedEventArgs"></a> Class RenderProcessTerminatedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Browser.IBrowser.RenderProcessTerminated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class RenderProcessTerminatedEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[RenderProcessTerminatedEventArgs](DotNetBrowser.Browser.Events.RenderProcessTerminatedEventArgs.md)

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

### <a id="DotNetBrowser_Browser_Events_RenderProcessTerminatedEventArgs_ExitCode"></a> ExitCode

Gets the render process exit code.

```csharp
public int ExitCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Browser_Events_RenderProcessTerminatedEventArgs_TerminationStatus"></a> TerminationStatus

Gets the status of the render process termination.

```csharp
public TerminationStatus TerminationStatus { get; }
```

#### Property Value

 [TerminationStatus](DotNetBrowser.Browser.Events.TerminationStatus.md)

## Methods

### <a id="DotNetBrowser_Browser_Events_RenderProcessTerminatedEventArgs_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

