# <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md)

#### Derived

[DefaultAuthenticationHandler](DotNetBrowser.WinForms.Dialogs.DefaultAuthenticationHandler.md), 
[DefaultStartDownloadHandler](DotNetBrowser.WinForms.Dialogs.DefaultStartDownloadHandler.md)

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Constructors

### <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase__ctor_System_Windows_Forms_Control_"></a> DialogHandlerBase\(Control\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(Control parent)
```

#### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

## Properties

### <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner window for the
modal dialogs.

```csharp
public Control Parent { get; }
```

#### Property Value

 [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

