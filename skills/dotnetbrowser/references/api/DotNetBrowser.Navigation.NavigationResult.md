# <a id="DotNetBrowser_Navigation_NavigationResult"></a> Class NavigationResult

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The result of the navigation occurred.

```csharp
public sealed class NavigationResult
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationResult](DotNetBrowser.Navigation.NavigationResult.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
    Use <xref href="DotNetBrowser.Navigation.NavigationResult.LoadResult" data-throw-if-not-resolved="false"></xref> to check whether the navigation has completed, failed, or stopped,
    and <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> to get the network error that caused the failure.
</p>
<p>
    The result does not contain the HTTP status code of the response. To check it, use
    <xref href="DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.ResponseCode" data-throw-if-not-resolved="false"></xref>.
</p>

## Properties

### <a id="DotNetBrowser_Navigation_NavigationResult_Error"></a> Error

Gets the network error associated with the navigation.

```csharp
public NetError? Error { get; }
```

#### Property Value

 [NetError](DotNetBrowser.Net.NetError.md)?

#### Remarks

<p>
    For <xref href="DotNetBrowser.Navigation.LoadResult.Completed" data-throw-if-not-resolved="false"></xref>, this property is always <code>null</code>.
</p>
<p>
    For <xref href="DotNetBrowser.Navigation.LoadResult.Failed" data-throw-if-not-resolved="false"></xref>, this property usually contains the network error
    that caused the failure. It is <code>null</code>, for example, when <xref href="DotNetBrowser.Navigation.INavigation.GoBack" data-throw-if-not-resolved="false"></xref> or
    <xref href="DotNetBrowser.Navigation.INavigation.GoForward" data-throw-if-not-resolved="false"></xref> is called and there is no entry to navigate to.
</p>
<p>
    For <xref href="DotNetBrowser.Navigation.LoadResult.Stopped" data-throw-if-not-resolved="false"></xref>, this property is either
    <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> or <code>null</code>.
</p>

### <a id="DotNetBrowser_Navigation_NavigationResult_LoadResult"></a> LoadResult

Gets the load result, which can be used to determine whether the navigation
has succeeded, failed, or stopped.

```csharp
public LoadResult LoadResult { get; }
```

#### Property Value

 [LoadResult](DotNetBrowser.Navigation.LoadResult.md)

