# <a id="DotNetBrowser_Browser_BrowserDisposeOptions"></a> Class BrowserDisposeOptions

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The dispose options of the browser.

```csharp
public sealed class BrowserDisposeOptions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserDisposeOptions](DotNetBrowser.Browser.BrowserDisposeOptions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_BrowserDisposeOptions_BeforeUnloadEventHandled"></a> BeforeUnloadEventHandled

Specifies whether the <code>beforeunload</code> and <code>unload</code> JavaScript events should be
handled if they are present on the web page loaded into the browser instance that is about to be disposed.

```csharp
public bool BeforeUnloadEventHandled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

