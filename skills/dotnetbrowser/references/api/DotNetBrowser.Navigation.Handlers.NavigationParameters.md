# <a id="DotNetBrowser_Navigation_Handlers_NavigationParameters"></a> Class NavigationParameters

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class NavigationParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NavigationParameters](DotNetBrowser.Navigation.Handlers.NavigationParameters.md)

#### Derived

[ShowHttpErrorPageParameters](DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageParameters.md), 
[ShowNetErrorPageParameters](DotNetBrowser.Navigation.Handlers.ShowNetErrorPageParameters.md), 
[StartNavigationParameters](DotNetBrowser.Navigation.Handlers.StartNavigationParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Handlers_NavigationParameters_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public INavigation Navigation { get; }
```

#### Property Value

 [INavigation](DotNetBrowser.Navigation.INavigation.md)

