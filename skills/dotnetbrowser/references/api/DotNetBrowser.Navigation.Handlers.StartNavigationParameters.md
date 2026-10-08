# <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters"></a> Class StartNavigationParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartNavigationParameters : NavigationParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.NavigationParameters.md) ← 
[StartNavigationParameters](DotNetBrowser.Navigation.Handlers.StartNavigationParameters.md)

#### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.NavigationParameters.md\#DotNetBrowser\_Navigation\_Handlers\_NavigationParameters\_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_HasUserGesture"></a> HasUserGesture

Indicates whether the navigation was initiated by a user gesture.

```csharp
public bool HasUserGesture { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsExternalProtocol"></a> IsExternalProtocol

Indicates whether the target URL cannot be handled by the browser's internal protocol
handlers.

```csharp
public bool IsExternalProtocol { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsMainFrame"></a> IsMainFrame

Indicates whether the navigation request URL belongs to a main frame.

```csharp
public bool IsMainFrame { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsPost"></a> IsPost

Indicates whether the navigation is done using HTTP POST method.

```csharp
public bool IsPost { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_IsRedirect"></a> IsRedirect

Indicates whether it's a redirect.

```csharp
public bool IsRedirect { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationParameters_Url"></a> Url

Gets the URL of the resource that will be loaded.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

