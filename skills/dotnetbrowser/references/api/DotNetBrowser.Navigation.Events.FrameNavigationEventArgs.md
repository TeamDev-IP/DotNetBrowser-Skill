# <a id="DotNetBrowser_Navigation_Events_FrameNavigationEventArgs"></a> Class FrameNavigationEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for all the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments containing
<xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public class FrameNavigationEventArgs : NavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md)

#### Derived

[FrameDocumentLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.FrameDocumentLoadFinishedEventArgs.md), 
[FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.FrameLoadFailedEventArgs.md), 
[FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.FrameLoadFinishedEventArgs.md), 
[NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.md)

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

### <a id="DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

