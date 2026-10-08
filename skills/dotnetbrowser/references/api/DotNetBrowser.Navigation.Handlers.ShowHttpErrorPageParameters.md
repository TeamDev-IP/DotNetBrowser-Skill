# <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters"></a> Class ShowHttpErrorPageParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowHttpErrorPageParameters : NavigationParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.NavigationParameters.md) ← 
[ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageParameters.md)

#### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.NavigationParameters.md\#DotNetBrowser\_Navigation\_Handlers\_NavigationParameters\_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters_HttpStatus"></a> HttpStatus

Gets the HTTP status code of the request.

```csharp
public HttpStatusCode HttpStatus { get; }
```

#### Property Value

 [HttpStatusCode](https://learn.microsoft.com/dotnet/api/system.net.httpstatuscode)

### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageParameters_Url"></a> Url

Gets the URL of the unreachable navigation request.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

