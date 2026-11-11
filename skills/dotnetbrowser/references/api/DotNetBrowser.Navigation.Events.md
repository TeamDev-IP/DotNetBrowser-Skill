# <a id="DotNetBrowser_Navigation_Events"></a> Namespace DotNetBrowser.Navigation.Events

### Classes

 [FrameDocumentLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameDocumentLoadFinishedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameDocumentLoadFinished" data-throw-if-not-resolved="false"></xref> event.

 [FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFailed" data-throw-if-not-resolved="false"></xref> event.

 [FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFinished" data-throw-if-not-resolved="false"></xref> event.

 [FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs)

The base class for all the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments containing
<xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

 [LoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadFinishedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadFinished" data-throw-if-not-resolved="false"></xref> event.

 [LoadProgressChangedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadProgressChanged" data-throw-if-not-resolved="false"></xref> event.

 [LoadStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadStartedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadStarted" data-throw-if-not-resolved="false"></xref> event.

 [NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs)

The base class for <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments.

 [NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationFinished" data-throw-if-not-resolved="false"></xref> event.

 [NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationRedirected" data-throw-if-not-resolved="false"></xref> event.

 [NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStartedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationStarted" data-throw-if-not-resolved="false"></xref> event.

 [NavigationStoppedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStoppedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationStopped" data-throw-if-not-resolved="false"></xref> event.

## <a id="DotNetBrowser_Navigation_Events_FrameDocumentLoadFinishedEventArgs"></a> Class FrameDocumentLoadFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameDocumentLoadFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class FrameDocumentLoadFinishedEventArgs : FrameNavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs) ← 
[FrameDocumentLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameDocumentLoadFinishedEventArgs)

##### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs"></a> Class FrameLoadFailedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFailed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class FrameLoadFailedEventArgs : FrameNavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs) ← 
[FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs)

##### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs_ErrorCode"></a> ErrorCode

Gets the network error code which is one from the <xref href="DotNetBrowser.Net.NetError" data-throw-if-not-resolved="false"></xref> enumeration.

```csharp
public NetError ErrorCode { get; }
```

##### Property Value

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)

#### <a id="DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs_ValidatedUrl"></a> ValidatedUrl

Gets the URL address which is failed to load.

```csharp
public string ValidatedUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs"></a> Class FrameLoadFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class FrameLoadFinishedEventArgs : FrameNavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs) ← 
[FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs)

##### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs_ValidatedUrl"></a> ValidatedUrl

Gets the URL address which is finished loading.

```csharp
public string ValidatedUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Events_FrameNavigationEventArgs"></a> Class FrameNavigationEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for all the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments containing
<xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public class FrameNavigationEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs)

##### Derived

[FrameDocumentLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameDocumentLoadFinishedEventArgs), 
[FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs), 
[FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs), 
[NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

## <a id="DotNetBrowser_Navigation_Events_LoadFinishedEventArgs"></a> Class LoadFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class LoadFinishedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[LoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadFinishedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs"></a> Class LoadProgressChangedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadProgressChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class LoadProgressChangedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[LoadProgressChangedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs_Progress"></a> Progress

Gets the value between 0 and 1 indicating the loading progress of the web page.

```csharp
public double Progress { get; }
```

##### Property Value

 [double](https://learn.microsoft.com/dotnet/api/system.double)

## <a id="DotNetBrowser_Navigation_Events_LoadStartedEventArgs"></a> Class LoadStartedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.LoadStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class LoadStartedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[LoadStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadStartedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs"></a> Class NavigationEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public class NavigationEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs)

##### Derived

[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs), 
[LoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadFinishedEventArgs), 
[LoadProgressChangedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs), 
[LoadStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadStartedEventArgs), 
[NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs), 
[NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStartedEventArgs), 
[NavigationStoppedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStoppedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance associated with the event.

```csharp
public INavigation Navigation { get; }
```

##### Property Value

 [INavigation](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigation)

## <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs"></a> Class NavigationFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationFinishedEventArgs : FrameNavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs) ← 
[NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs)

##### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameNavigationEventArgs_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_ErrorCode"></a> ErrorCode

Gets the navigation error code.

```csharp
public NetError ErrorCode { get; }
```

##### Property Value

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_HasCommitted"></a> HasCommitted

Indicates whether the navigation has committed.

```csharp
public bool HasCommitted { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_IsErrorPage"></a> IsErrorPage

Indicates whether the navigation resulted in an error page.

```csharp
public bool IsErrorPage { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_IsSameDocument"></a> IsSameDocument

Indicates whether the navigation has been performed in the scope of the same document.

```csharp
public bool IsSameDocument { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_ResponseCode"></a> ResponseCode

The HTTP status code returned by the server in response to the navigation request.

```csharp
public int ResponseCode { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

This property is populated when the navigation results in a response that includes valid
response headers.

<p>
    <b>This includes the following cases:</b>
</p>
<ul><li>
            The server returns HTTP(S) response headers with a status code (e.g., 200, 404).
        </li><li>
            Chromium creates a synthetic response header for a well-formed <code>data:</code> URL
            (for example, <code>data:,Hello</code>). In this case, the status code is typically 200 (OK).
        </li><li>
            Chromium creates a response header for a valid <code>file:</code> URL if the file exists,
            also typically with status code 200 (OK).
        </li></ul>

If the navigation does not result in a response with headers, this field is set to 0.

<p>
    <b>This includes the following cases:</b>
</p>
<ul><li>
            The navigation failed at the network level (e.g., DNS failure, timeout, connection refused, offline).
        </li><li>
            The navigation failed due to invalid scheme target URLs:

<ul><li>
                        Malformed <code>data:</code> URLs (e.g., missing comma or invalid format). No synthetic header is
                        created.
                    </li><li>
                        <code>file:</code> URL for a file that does not exist. No synthetic header is created.
                    </li></ul>
        </li><li>
            The target URL uses a scheme that does not involve an HTTP(S) response and therefore
            does not produce response headers, including:

<ul><li><code>about:</code> (e.g., <code>about:blank</code>)</li><li><code>chrome:</code>, <code>chrome-extension:</code> (internal browser/extension pages)</li></ul>
        </li><li>
            The navigation was performed within the same document:

<ul><li>Fragment navigations (e.g., navigating to <code>#anchor</code>)</li><li>History API navigations (e.g., <code>pushState</code>, <code>replaceState</code>)</li></ul>
        </li></ul>
<p>
    <b>Note:</b> A value of <code>0</code> does <b>not</b> mean the server responded with HTTP status code 0.
    It means that the HTTP status code could not be determined because no HTTP-level response occurred
    or no synthetic response was generated for the navigation.
</p>

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_Url"></a> Url

Gets the navigation URL.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_WasServerRedirect"></a> WasServerRedirect

Indicates whether the navigation has encountered a server redirect.

```csharp
public bool WasServerRedirect { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs"></a> Class NavigationRedirectedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationRedirected" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationRedirectedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs_Url"></a> Url

Gets the destination URL for the navigation redirect.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs"></a> Class NavigationStartedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationStartedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStartedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_IsMainFrame"></a> IsMainFrame

Indicates whether the navigation is started in the main frame.

```csharp
public bool IsMainFrame { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_IsSameDocument"></a> IsSameDocument

Indicates whether the navigation will be performed in the scope of the same document.

```csharp
public bool IsSameDocument { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Events_NavigationStartedEventArgs_Url"></a> Url

Gets the URL of the navigation.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Events_NavigationStoppedEventArgs"></a> Class NavigationStoppedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationStopped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationStoppedEventArgs : NavigationEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs) ← 
[NavigationStoppedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStoppedEventArgs)

##### Inherited Members

[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationEventArgs_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)
