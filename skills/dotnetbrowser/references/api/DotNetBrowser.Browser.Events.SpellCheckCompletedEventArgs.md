# <a id="DotNetBrowser_Browser_Events_SpellCheckCompletedEventArgs"></a> Class SpellCheckCompletedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Browser.IBrowser.SpellCheckCompleted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class SpellCheckCompletedEventArgs : FrameEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[FrameEventArgs](DotNetBrowser.Browser.Events.FrameEventArgs.md) ← 
[SpellCheckCompletedEventArgs](DotNetBrowser.Browser.Events.SpellCheckCompletedEventArgs.md)

#### Inherited Members

[FrameEventArgs.Frame](DotNetBrowser.Browser.Events.FrameEventArgs.md\#DotNetBrowser\_Browser\_Events\_FrameEventArgs\_Frame), 
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

### <a id="DotNetBrowser_Browser_Events_SpellCheckCompletedEventArgs_CheckedText"></a> CheckedText

Gets the text that has been checked by the spell checker.

```csharp
public string CheckedText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Events_SpellCheckCompletedEventArgs_Results"></a> Results

Gets the collection of the spell checking results.

```csharp
public IEnumerable<SpellCheckingResult> Results { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[SpellCheckingResult](DotNetBrowser.SpellCheck.SpellCheckingResult.md)\>

