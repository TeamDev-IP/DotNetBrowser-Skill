# <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters"></a> Class ShowNetErrorPageParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowNetErrorPageParameters : NavigationParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.NavigationParameters.md) ← 
[ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.ShowNetErrorPageParameters.md)

#### Inherited Members

[NavigationParameters.Navigation](DotNetBrowser.Navigation.Handlers.NavigationParameters.md\#DotNetBrowser\_Navigation\_Handlers\_NavigationParameters\_Navigation), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters_NetError"></a> NetError

Gets the URL request error code.

```csharp
public NetError NetError { get; }
```

#### Property Value

 [NetError](DotNetBrowser.Net.NetError.md)

### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageParameters_Url"></a> Url

Gets the URL of the unreachable navigation request.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

