# <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadParameters"></a> Class BeforeUnloadParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for common dialog parameters.

```csharp
public sealed class BeforeUnloadParameters : CommonDialogParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[CommonDialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md) ← 
[BeforeUnloadParameters](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadParameters.md)

#### Inherited Members

[CommonDialogParameters.Message](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_CommonDialogParameters\_Message), 
[CommonDialogParameters.Title](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_CommonDialogParameters\_Title), 
[DialogParameters.Browser](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_DialogParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadParameters_Cause"></a> Cause

Gets the action that caused the dialog to appear.

```csharp
public BeforeUnloadCause Cause { get; }
```

#### Property Value

 [BeforeUnloadCause](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadCause.md)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadParameters_LeaveActionText"></a> LeaveActionText

The localized text of the "Leave" action.

```csharp
public string LeaveActionText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadParameters_StayActionText"></a> StayActionText

Gets the localized text of the "Stay" action.

```csharp
public string StayActionText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

