# <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs"></a> Class FrameLoadFailedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFailed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class FrameLoadFailedEventArgs : FrameNavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md) ← 
[FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.FrameLoadFailedEventArgs.md)

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

### <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs_ErrorCode"></a> ErrorCode

Gets the network error code which is one from the <xref href="DotNetBrowser.Net.NetError" data-throw-if-not-resolved="false"></xref> enumeration.

```csharp
public NetError ErrorCode { get; }
```

#### Property Value

 [NetError](DotNetBrowser.Net.NetError.md)

### <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs_ValidatedUrl"></a> ValidatedUrl

Gets the URL address which is failed to load.

```csharp
public string ValidatedUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

