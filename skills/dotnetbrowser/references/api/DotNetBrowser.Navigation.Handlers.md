# <a id="DotNetBrowser_Navigation_Handlers"></a> Namespace DotNetBrowser.Navigation.Handlers

### Classes

 [NavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters)

The base class for all <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> handlers parameters.

 [ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters)

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

 [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse)

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

 [ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters)

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

 [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse)

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

 [StartNavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationParameters)

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

 [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationResponse)

A response to the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Navigation_Handlers_NavigationParameters"></a> Class NavigationParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class NavigationParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters)

##### Derived

[ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters), 
[ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters), 
[StartNavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Handlers_NavigationParameters_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public INavigation Navigation { get; }
```

##### Property Value

 [INavigation](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigation)

## <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters"></a> Class ShowHttpErrorPageParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowHttpErrorPageParameters : NavigationParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters) ← 
[ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters)

##### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters_HttpStatus"></a> HttpStatus

Gets the HTTP status code of the request.

```csharp
public HttpStatusCode HttpStatus { get; }
```

##### Property Value

 [HttpStatusCode](https://learn.microsoft.com/dotnet/api/system.net.httpstatuscode)

#### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters_Url"></a> Url

Gets the URL of the unreachable navigation request.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse"></a> Class ShowHttpErrorPageResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowHttpErrorPageResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse_Show_System_String_"></a> Show\(string\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display an error page
with the specified <code class="paramref">errorHtml</code>.

```csharp
public static ShowHttpErrorPageResponse Show(string errorHtml)
```

##### Parameters

`errorHtml` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML code of the error page to display.

##### Returns

 [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">errorHtml</code> is null, empty, or contains only white space.

#### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse_ShowDefault"></a> ShowDefault\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display
the default error page.

```csharp
public static ShowHttpErrorPageResponse ShowDefault()
```

##### Returns

 [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters"></a> Class ShowNetErrorPageParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowNetErrorPageParameters : NavigationParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters) ← 
[ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters)

##### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters_NetError"></a> NetError

Gets the URL request error code.

```csharp
public NetError NetError { get; }
```

##### Property Value

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)

#### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters_Url"></a> Url

Gets the URL of the unreachable navigation request.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse"></a> Class ShowNetErrorPageResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowNetErrorPageResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse_Show_System_String_"></a> Show\(string\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display an error page
with the specified <code class="paramref">errorHtml</code>.

```csharp
public static ShowNetErrorPageResponse Show(string errorHtml)
```

##### Parameters

`errorHtml` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML code of the error page to display.

##### Returns

 [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">errorHtml</code> is null, empty, or contains only white space.

#### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse_ShowDefault"></a> ShowDefault\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display
the default error page.

```csharp
public static ShowNetErrorPageResponse ShowDefault()
```

##### Returns

 [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters"></a> Class StartNavigationParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartNavigationParameters : NavigationParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters) ← 
[StartNavigationParameters](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationParameters)

##### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_NavigationParameters_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_HasUserGesture"></a> HasUserGesture

Indicates whether the navigation was initiated by a user gesture.

```csharp
public bool HasUserGesture { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsExternalProtocol"></a> IsExternalProtocol

Indicates whether the target URL cannot be handled by the browser's internal protocol
handlers.

```csharp
public bool IsExternalProtocol { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsMainFrame"></a> IsMainFrame

Indicates whether the navigation request URL belongs to a main frame.

```csharp
public bool IsMainFrame { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsPost"></a> IsPost

Indicates whether the navigation is done using HTTP POST method.

```csharp
public bool IsPost { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsRedirect"></a> IsRedirect

Indicates whether it's a redirect.

```csharp
public bool IsRedirect { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_Url"></a> Url

Gets the URL of the resource that will be loaded.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse"></a> Class StartNavigationResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartNavigationResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartNavigationResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse_Ignore"></a> Ignore\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the load request should be ignored.

```csharp
public static StartNavigationResponse Ignore()
```

##### Returns

 [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse_Start"></a> Start\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should continue loading the URL.

```csharp
public static StartNavigationResponse Start()
```

##### Returns

 [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.md#DotNetBrowser_Navigation_Handlers_StartNavigationResponse)

The <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref> implementation.
