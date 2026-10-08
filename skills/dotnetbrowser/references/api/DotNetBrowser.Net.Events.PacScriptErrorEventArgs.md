# <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs"></a> Class PacScriptErrorEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.PacScriptErrorOccurred" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class PacScriptErrorEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PacScriptErrorEventArgs](DotNetBrowser.Net.Events.PacScriptErrorEventArgs.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs_ErrorText"></a> ErrorText

Gets the ErrorText.

```csharp
public string ErrorText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs_LineNumber"></a> LineNumber

Gets the LineNumber which contains the error.

```csharp
public uint LineNumber { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

