# <a id="DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs"></a> Class FrameLoadFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class FrameLoadFinishedEventArgs : FrameNavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md) ← 
[FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.FrameLoadFinishedEventArgs.md)

#### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_FrameNavigationEventArgs\_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.NavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_NavigationEventArgs\_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.NavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_NavigationEventArgs\_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs_ValidatedUrl"></a> ValidatedUrl

Gets the URL address which is finished loading.

```csharp
public string ValidatedUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

