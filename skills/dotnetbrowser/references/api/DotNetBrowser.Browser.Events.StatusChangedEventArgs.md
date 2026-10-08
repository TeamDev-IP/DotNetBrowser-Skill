# <a id="DotNetBrowser_Browser_Events_StatusChangedEventArgs"></a> Class StatusChangedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Browser.IBrowser.StatusChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class StatusChangedEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[StatusChangedEventArgs](DotNetBrowser.Browser.Events.StatusChangedEventArgs.md)

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

### <a id="DotNetBrowser_Browser_Events_StatusChangedEventArgs_Text"></a> Text

Gets the new status text.

```csharp
public string Text { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Events_StatusChangedEventArgs_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

