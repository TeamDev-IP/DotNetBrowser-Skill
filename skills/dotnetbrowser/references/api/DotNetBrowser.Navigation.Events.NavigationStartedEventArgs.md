# <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs"></a> Class NavigationStartedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationStartedEventArgs : NavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.NavigationStartedEventArgs.md)

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

### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_IsMainFrame"></a> IsMainFrame

Indicates whether the navigation is started in the main frame.

```csharp
public bool IsMainFrame { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_IsSameDocument"></a> IsSameDocument

Indicates whether the navigation will be performed in the scope of the same document.

```csharp
public bool IsSameDocument { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_Url"></a> Url

Gets the URL of the navigation.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

