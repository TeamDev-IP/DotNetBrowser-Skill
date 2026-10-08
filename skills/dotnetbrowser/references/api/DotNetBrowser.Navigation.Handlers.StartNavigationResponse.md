# <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse"></a> Class StartNavigationResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartNavigationResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartNavigationResponse](DotNetBrowser.Navigation.Handlers.StartNavigationResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse_Ignore"></a> Ignore\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the load request should be ignored.

```csharp
public static StartNavigationResponse Ignore()
```

#### Returns

 [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.StartNavigationResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Navigation_Handlers_StartNavigationResponse_Start"></a> Start\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should continue loading the URL.

```csharp
public static StartNavigationResponse Start()
```

#### Returns

 [StartNavigationResponse](DotNetBrowser.Navigation.Handlers.StartNavigationResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.StartNavigationResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.StartNavigationHandler" data-throw-if-not-resolved="false"></xref> implementation.

