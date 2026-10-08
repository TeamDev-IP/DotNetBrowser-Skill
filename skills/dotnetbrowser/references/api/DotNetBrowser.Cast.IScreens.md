# <a id="DotNetBrowser_Cast_IScreens"></a> Interface IScreens

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The service that allows obtaining connected screens whose content can be cast.

```csharp
public interface IScreens
```

## Properties

### <a id="DotNetBrowser_Cast_IScreens_All"></a> All

Gets the list of connected screens whose content can be cast to a media receiver.

```csharp
IReadOnlyList<Screen> All { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Screen](DotNetBrowser.Cast.Screen.md)\>

### <a id="DotNetBrowser_Cast_IScreens_DefaultScreen"></a> DefaultScreen

Gets the default (main) screen.

```csharp
Screen DefaultScreen { get; }
```

#### Property Value

 [Screen](DotNetBrowser.Cast.Screen.md)

