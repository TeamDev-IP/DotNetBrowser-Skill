# <a id="DotNetBrowser_Navigation_LoadResult"></a> Enum LoadResult

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The loading result.

```csharp
public enum LoadResult
```

## Fields

`Completed = 0` 

The page loading has completed.

The navigation has finished without a network error, or a same-document navigation, such as
navigating to an anchor, has been committed. <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> is <code>null</code>.

`Failed = 1` 

The page loading has failed.

<p>
    The navigation has failed with a network error other than <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref>,
    or an error page has been committed instead of the requested page.
    In these cases, <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> contains the network error.
</p>
<p>
    <xref href="DotNetBrowser.Navigation.INavigation.GoBack" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Navigation.INavigation.GoForward" data-throw-if-not-resolved="false"></xref> also return this result,
    with <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> set to <code>null</code>, when there is no entry to navigate to.
</p>

`Stopped = 2` 

The page loading has stopped.

The navigation has been aborted with the <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> error, for example,
because <xref href="DotNetBrowser.Navigation.INavigation.Stop" data-throw-if-not-resolved="false"></xref> has been called. <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> is
either <xref href="DotNetBrowser.Net.NetError.Aborted" data-throw-if-not-resolved="false"></xref> or <code>null</code>.

## Remarks

<p>
    <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> does not provide the HTTP status code of the response. To check
    it, use <xref href="DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.ResponseCode" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    If the navigation does not finish within the timeout, the navigation task throws
    <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref> instead of returning a result.
</p>

