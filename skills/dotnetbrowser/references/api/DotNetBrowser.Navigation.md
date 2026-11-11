# <a id="DotNetBrowser_Navigation"></a> Namespace DotNetBrowser.Navigation

### Namespaces

 [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)

 [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)

### Classes

 [LoadUrlParameters](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadUrlParameters)

The parameters of the load url request.

 [NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)

The result of the navigation occurred.

### Interfaces

 [INavigation](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigation)

Allows loading resources in the browser instance and working with the navigation history.

 [INavigationEntry](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigationEntry)

The navigation history entry.

### Enums

 [LoadResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadResult)

The loading result.

 [PageType](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_PageType)

Represents a navigation page type.

## <a id="DotNetBrowser_Navigation_LoadUrlParameters"></a> Class LoadUrlParameters

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The parameters of the load url request.

```csharp
public sealed class LoadUrlParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[LoadUrlParameters](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadUrlParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Navigation_LoadUrlParameters__ctor_System_String_"></a> LoadUrlParameters\(string\)

Initializes a new instance of <xref href="DotNetBrowser.Navigation.LoadUrlParameters" data-throw-if-not-resolved="false"></xref> with the specified <code class="paramref">url</code>.

```csharp
public LoadUrlParameters(string url)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty or contain only white space.

### Properties

#### <a id="DotNetBrowser_Navigation_LoadUrlParameters_HttpHeaders"></a> HttpHeaders

Gets or sets the HTTP headers that will be sent with the request.

```csharp
public IEnumerable<HttpHeader> HttpHeaders { get; set; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.md#DotNetBrowser_Net_HttpHeader)\>

##### Remarks

Setting certain forbidden headers (such as 'Referer', 'Host', 'Content-Length', 'Keep-Alive', 'Proxy-headers',
'TE', etc.) will have no effect due to browser security restrictions. These headers are controlled by the browser and
cannot be set for <xref href="DotNetBrowser.Navigation.LoadUrlParameters" data-throw-if-not-resolved="false"></xref> for security reasons.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null or contains null items.

#### <a id="DotNetBrowser_Navigation_LoadUrlParameters_UploadData"></a> UploadData

Gets or sets the POST upload data that will be sent with the request.

```csharp
public UploadData UploadData { get; set; }
```

##### Property Value

 [UploadData](DotNetBrowser.Net.md#DotNetBrowser_Net_UploadData)

#### <a id="DotNetBrowser_Navigation_LoadUrlParameters_Url"></a> Url

Gets the URL of the resource to load.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_NavigationResult"></a> Class NavigationResult

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The result of the navigation occurred.

```csharp
public sealed class NavigationResult
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    Use <xref href="DotNetBrowser.Navigation.NavigationResult.LoadResult" data-throw-if-not-resolved="false"></xref> to check whether the navigation has completed, failed, or stopped,
    and <xref href="DotNetBrowser.Navigation.NavigationResult.Error" data-throw-if-not-resolved="false"></xref> to get the network error that caused the failure.
</p>
<p>
    The result does not contain the HTTP status code of the response. To check it, use
    <xref href="DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.ResponseCode" data-throw-if-not-resolved="false"></xref>.
</p>

### Properties

#### <a id="DotNetBrowser_Navigation_NavigationResult_Error"></a> Error

Gets the network error associated with the navigation.

```csharp
public NetError? Error { get; }
```

##### Property Value

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)?

##### Remarks

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

#### <a id="DotNetBrowser_Navigation_NavigationResult_LoadResult"></a> LoadResult

Gets the load result, which can be used to determine whether the navigation
has succeeded, failed, or stopped.

```csharp
public LoadResult LoadResult { get; }
```

##### Property Value

 [LoadResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadResult)

## <a id="DotNetBrowser_Navigation_INavigation"></a> Interface INavigation

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

Allows loading resources in the browser instance and working with the navigation history.

```csharp
public interface INavigation : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Navigation_INavigation_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Navigation_INavigation_CurrentEntry"></a> CurrentEntry

Gets the current navigation item in the back-forward list.

```csharp
INavigationEntry CurrentEntry { get; }
```

##### Property Value

 [INavigationEntry](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigationEntry)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Navigation_INavigation_CurrentIndex"></a> CurrentIndex

Gets the index of the current navigation item in the back-forward list.

```csharp
int CurrentIndex { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Navigation_INavigation_EntryCount"></a> EntryCount

Gets the number of items in the back-forward list.

```csharp
int EntryCount { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Navigation_INavigation_ShowHttpErrorPageHandler"></a> ShowHttpErrorPageHandler

Gets or sets a handler that is used when the engine is about to display an error web page because the web
server sends an empty HTTP response with the HTTP status code that represents an error.

```csharp
IHandler<ShowHttpErrorPageParameters, ShowHttpErrorPageResponse> ShowHttpErrorPageHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters), [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse)\>

##### Remarks

<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.Show(System.String)" data-throw-if-not-resolved="false"></xref> to show the custom error page with the given HTML.
</p>
<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.ShowDefault" data-throw-if-not-resolved="false"></xref> to display the default Chromium error page.
</p>
<p>
    <b>Important:</b> the engine will be blocked until the <code>Handle()</code> method returns.
    It is not allowed to invoke any engine methods
    in the scope of this handler implementation.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_ShowNetErrorPageHandler"></a> ShowNetErrorPageHandler

Gets or sets a handler that is used when the engine is about to display a network error web page because the
required web resource cannot be loaded because of a network error.

```csharp
IHandler<ShowNetErrorPageParameters, ShowNetErrorPageResponse> ShowNetErrorPageHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters), [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse)\>

##### Remarks

<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.Show(System.String)" data-throw-if-not-resolved="false"></xref> to show the custom network error page with the given HTML.
</p>
<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.ShowDefault" data-throw-if-not-resolved="false"></xref> to display the default Chromium network error page.
</p>
<p>
    <b>Important:</b> the engine will be blocked until the <code>Handle()</code> method returns.
    It is not allowed to invoke any engine methods
    in the scope of this handler implementation.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_StartNavigationHandler"></a> StartNavigationHandler

Gets or sets a handler that is used before the browser starts navigation to a resource.

```csharp
IHandler<StartNavigationParameters, StartNavigationResponse> StartNavigationHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[StartNavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationParameters), [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationResponse)\>

##### Remarks

<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse.Start" data-throw-if-not-resolved="false"></xref> to allow navigation start.
</p>
<p>
    Use <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse.Ignore" data-throw-if-not-resolved="false"></xref> to ignore navigation request.
</p>
<p>
    <b>Important:</b> the browser will be blocked until the <code>Handle()</code> method returns.
    It is not allowed to invoke any browser methods in the scope of this handler implementation.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Navigation_INavigation_CanGoBack"></a> CanGoBack\(\)

Checks whether the previous location can be loaded.

```csharp
bool CanGoBack()
```

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the previous location in the back-forward list can be loaded.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_CanGoForward"></a> CanGoForward\(\)

Checks whether the next location can be loaded.

```csharp
bool CanGoForward()
```

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the next location in the back-forward list can be loaded.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_EntryAt_System_Int32_"></a> EntryAt\(int\)

Returns an <xref href="DotNetBrowser.Navigation.INavigationEntry" data-throw-if-not-resolved="false"></xref> instance for the given <code>index</code>
in the back-forward list.

```csharp
INavigationEntry EntryAt(int index)
```

##### Parameters

`index` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The location of the item to return in the back-forward list.

##### Returns

 [INavigationEntry](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigationEntry)

The navigation entry that corresponds to the index.

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The <code class="paramref">index</code> is less than 0 or more than the number of items in the
back-forward list.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_GoBack"></a> GoBack\(\)

Loads the previous location in the back-forward list. It does nothing if there's no previous location in the list.

```csharp
Task<NavigationResult> GoBack()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous navigation operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the navigation operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the navigation operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_GoForward"></a> GoForward\(\)

Loads the next location in the back-forward list. It does nothing if there's no next location in the list.

```csharp
Task<NavigationResult> GoForward()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous navigation operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the navigation operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the navigation operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_GoTo_System_Int32_"></a> GoTo\(int\)

Navigates to a specific location at the given <code class="paramref">index</code> in the back-forward list.

```csharp
Task<NavigationResult> GoTo(int index)
```

##### Parameters

`index` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The location of the item to load in the back-forward list.
Cannot be negative or more than the number of items in the back-forward list.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous navigation operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the navigation operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the navigation operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The <code class="paramref">index</code> is less than 0 or more than the
number of items in the back-forward list.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadUrl_System_String_"></a> LoadUrl\(string\)

Navigates to a resource identified by a URL.

```csharp
Task<NavigationResult> LoadUrl(string url)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code>is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadUrl_System_String_System_TimeSpan_"></a> LoadUrl\(string, TimeSpan\)

Navigates to a resource identified by a URL, with the specified <code class="paramref">timeout</code>.

```csharp
Task<NavigationResult> LoadUrl(string url, TimeSpan timeout)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The timeout for the loading operation.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a <code class="paramref">timeout</code>.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadUrl_DotNetBrowser_Navigation_LoadUrlParameters_"></a> LoadUrl\(LoadUrlParameters\)

Navigates to a resource identified by the specified <code class="paramref">parameters</code>

```csharp
Task<NavigationResult> LoadUrl(LoadUrlParameters parameters)
```

##### Parameters

`parameters` [LoadUrlParameters](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadUrlParameters)

The parameters such as URL, POST data, and HTTP headers.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">parameters</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadUrl_DotNetBrowser_Navigation_LoadUrlParameters_System_TimeSpan_"></a> LoadUrl\(LoadUrlParameters, TimeSpan\)

Navigates to a resource identified by the given <xref href="DotNetBrowser.Navigation.LoadUrlParameters" data-throw-if-not-resolved="false"></xref>, with the specified timout.

```csharp
Task<NavigationResult> LoadUrl(LoadUrlParameters parameters, TimeSpan timeout)
```

##### Parameters

`parameters` [LoadUrlParameters](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_LoadUrlParameters)

The parameters such as URL, POST data, and HTTP headers.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The timeout for the loading operation.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a <code class="paramref">timeout</code>.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">parameters</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_Reload"></a> Reload\(\)

Reloads the currently loaded web page.

```csharp
Task<NavigationResult> Reload()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous reloading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the reloading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the reloading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_ReloadAndCheckForRepost"></a> ReloadAndCheckForRepost\(\)

Reloads the currently loaded web page.
If the current web page has POST data, the user will be
asked to confirm that he really wants to reload the page.

```csharp
Task<NavigationResult> ReloadAndCheckForRepost()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous reloading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the reloading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the reloading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_ReloadIgnoringCache"></a> ReloadIgnoringCache\(\)

Reloads the currently loaded web page ignoring the cached data.

```csharp
Task<NavigationResult> ReloadIgnoringCache()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous reloading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the reloading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the reloading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_ReloadIgnoringCacheAndCheckForRepost"></a> ReloadIgnoringCacheAndCheckForRepost\(\)

Reloads the currently loaded web page ignoring the cached data.
If the current web page has POST data, the user will be
asked to confirm that he really wants to reload the page.

```csharp
Task<NavigationResult> ReloadIgnoringCacheAndCheckForRepost()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous reloading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the reloading operation has been completed, stopped or failed.
The task can throw <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the reloading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_RemoveEntryAt_System_Int32_"></a> RemoveEntryAt\(int\)

Removes the item at the given <code class="paramref">index</code> from the back-forward list
and returns true if it was removed successfully.

```csharp
bool RemoveEntryAt(int index)
```

##### Parameters

`index` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The location of the item to remove in the back-forward list.
Cannot be negative, point to the current item, or more than the number of items in the back-forward list.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

returns true if the item was removed successfully.

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

The <code class="paramref">index</code> is less than 0 or more than the
number of items in the back-forward list.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_Stop"></a> Stop\(\)

Cancels any pending navigation or download operation and stops any dynamic page
elements, such as background sounds and animations.

```csharp
void Stop()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_FrameDocumentLoadFinished"></a> FrameDocumentLoadFinished

Occurs when the document loading in the given <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been finished. At this point,
deferred scripts were executed, and content scripts marked "document_end" get injected into the
<xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
event EventHandler<FrameDocumentLoadFinishedEventArgs> FrameDocumentLoadFinished
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameDocumentLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameDocumentLoadFinishedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_FrameLoadFailed"></a> FrameLoadFailed

Occurs when the content load was failed.

```csharp
event EventHandler<FrameLoadFailedEventArgs> FrameLoadFailed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameLoadFailedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFailedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_FrameLoadFinished"></a> FrameLoadFinished

Occurs when the content of the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been loaded completely.

```csharp
event EventHandler<FrameLoadFinishedEventArgs> FrameLoadFinished
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameLoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_FrameLoadFinishedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadFinished"></a> LoadFinished

Occurs when the content loading has been finished. This event corresponds to the
moment when the spinner of the tab stops spinning.

```csharp
event EventHandler<LoadFinishedEventArgs> LoadFinished
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[LoadFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadFinishedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadProgressChanged"></a> LoadProgressChanged

Occurs when the page has made some progress loading.

```csharp
event EventHandler<LoadProgressChangedEventArgs> LoadProgressChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[LoadProgressChangedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadProgressChangedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_LoadStarted"></a> LoadStarted

Occurs when the content loading has been started.
This event corresponds to the moment when the spinner of the tab starts spinning.

```csharp
event EventHandler<LoadStartedEventArgs> LoadStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[LoadStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_LoadStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_NavigationFinished"></a> NavigationFinished

Occurs when the navigation has been finished. This happens when a navigation is
committed, aborted, or replaced by a new one.

```csharp
event EventHandler<NavigationFinishedEventArgs> NavigationFinished
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_NavigationRedirected"></a> NavigationRedirected

Occurs when the navigation has encountered a server redirect.

```csharp
event EventHandler<NavigationRedirectedEventArgs> NavigationRedirected
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[NavigationRedirectedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationRedirectedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_NavigationStarted"></a> NavigationStarted

Occurs when the navigation has been started. This is also fired by same-document navigations,
such as fragment navigations or pushState/replaceState, which will not result in a
document change. To filter these out, use the <xref href="DotNetBrowser.Navigation.Events.NavigationStartedEventArgs.IsSameDocument" data-throw-if-not-resolved="false"></xref> property.

<p>
    Note that more than one navigation can be ongoing in the same frame at the same time(including
    the main frame). Also, there is no guarantee that the <xref href="DotNetBrowser.Navigation.INavigation.NavigationFinished" data-throw-if-not-resolved="false"></xref> will be fired for
    any particular navigation before this event is called on the next.
</p>

```csharp
event EventHandler<NavigationStartedEventArgs> NavigationStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[NavigationStartedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Navigation_INavigation_NavigationStopped"></a> NavigationStopped

Occurs when the navigation has been stopped.

```csharp
event EventHandler<NavigationStoppedEventArgs> NavigationStopped
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[NavigationStoppedEventArgs](DotNetBrowser.Navigation.Events.md#DotNetBrowser_Navigation_Events_NavigationStoppedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Navigation_INavigationEntry"></a> Interface INavigationEntry

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The navigation history entry.

```csharp
public interface INavigationEntry
```

### Properties

#### <a id="DotNetBrowser_Navigation_INavigationEntry_HttpStatusCode"></a> HttpStatusCode

Gets the status code of the last known successful navigation.

```csharp
int HttpStatusCode { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Navigation_INavigationEntry_OriginalRequestUrl"></a> OriginalRequestUrl

Gets the URL that caused this entry to be created.

```csharp
string OriginalRequestUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Navigation_INavigationEntry_PageType"></a> PageType

Gets the page type that tells if this entry is for an interstitial or error page.

```csharp
PageType PageType { get; }
```

##### Property Value

 [PageType](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_PageType)

#### <a id="DotNetBrowser_Navigation_INavigationEntry_Timestamp"></a> Timestamp

Gets the time at which the last known local navigation was completed.

```csharp
DateTime? Timestamp { get; }
```

##### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

#### <a id="DotNetBrowser_Navigation_INavigationEntry_Title"></a> Title

Gets the title as set by the page. This value is empty if there is no title set.

```csharp
string Title { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Navigation_INavigationEntry_Url"></a> Url

Gets the actual URL of the web page.

```csharp
string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_LoadResult"></a> Enum LoadResult

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The loading result.

```csharp
public enum LoadResult
```

### Fields

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

### Remarks

<p>
    <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> does not provide the HTTP status code of the response. To check
    it, use <xref href="DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.ResponseCode" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    If the navigation does not finish within the timeout, the navigation task throws
    <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref> instead of returning a result.
</p>

## <a id="DotNetBrowser_Navigation_PageType"></a> Enum PageType

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

Represents a navigation page type.

```csharp
public enum PageType
```

### Fields

`Error = 2` 

Error page.



`Normal = 1` 

Normal page.
