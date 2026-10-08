# <a id="DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs"></a> Class NavigationRedirectedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationRedirected" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationRedirectedEventArgs : NavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.NavigationRedirectedEventArgs.md)

#### Inherited Members

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

### <a id="DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs_Url"></a> Url

Gets the destination URL for the navigation redirect.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

