# <a id="DotNetBrowser_Wpf_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.Wpf.Dialogs](DotNetBrowser.Wpf.Dialogs.md)  
Assembly: DotNetBrowser.Wpf.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.Wpf.Dialogs.DialogHandlerBase.md)

#### Derived

[DefaultAuthenticationHandler](DotNetBrowser.Wpf.Dialogs.DefaultAuthenticationHandler.md), 
[DefaultStartDownloadHandler](DotNetBrowser.Wpf.Dialogs.DefaultStartDownloadHandler.md)

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Constructors

### <a id="DotNetBrowser_Wpf_Dialogs_DialogHandlerBase__ctor_System_Windows_DependencyObject_"></a> DialogHandlerBase\(DependencyObject\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(DependencyObject parent)
```

#### Parameters

`parent` [DependencyObject](https://learn.microsoft.com/dotnet/api/system.windows.dependencyobject)

The parent object for the dialog displayed by this handler.

## Properties

### <a id="DotNetBrowser_Wpf_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner window for the
modal dialogs.

```csharp
public DependencyObject Parent { get; }
```

#### Property Value

 [DependencyObject](https://learn.microsoft.com/dotnet/api/system.windows.dependencyobject)

