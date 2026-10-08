# <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs"></a> Class NavigationEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public class NavigationEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md)

#### Derived

[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md), 
[LoadFinishedEventArgs](DotNetBrowser.Navigation.Events.LoadFinishedEventArgs.md), 
[LoadProgressChangedEventArgs](DotNetBrowser.Navigation.Events.LoadProgressChangedEventArgs.md), 
[LoadStartedEventArgs](DotNetBrowser.Navigation.Events.LoadStartedEventArgs.md), 
[NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.NavigationRedirectedEventArgs.md), 
[NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.NavigationStartedEventArgs.md), 
[NavigationStoppedEventArgs](DotNetBrowser.Navigation.Events.NavigationStoppedEventArgs.md)

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

### <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public INavigation Navigation { get; }
```

#### Property Value

 [INavigation](DotNetBrowser.Navigation.INavigation.md)

