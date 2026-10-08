# <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs"></a> Class ConsoleMessageReceivedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Browser.IBrowser.ConsoleMessageReceived" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class ConsoleMessageReceivedEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[ConsoleMessageReceivedEventArgs](DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.md)

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

### <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs_Level"></a> Level

Gets the console message level.

```csharp
public ConsoleMessageReceivedEventArgs.MessageLevel Level { get; }
```

#### Property Value

 [ConsoleMessageReceivedEventArgs](DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.md).[MessageLevel](DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.MessageLevel.md)

### <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs_LineNumber"></a> LineNumber

Gets the line number that caused the message.

```csharp
public int LineNumber { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs_Message"></a> Message

Gets the console message text.

```csharp
public string Message { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs_Source"></a> Source

Gets the source of the console message.

```csharp
public string Source { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

