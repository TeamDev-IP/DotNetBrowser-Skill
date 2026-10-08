# <a id="DotNetBrowser_Browser_Dialogs_Handlers_AlertParameters"></a> Class AlertParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for common dialog parameters.

```csharp
public sealed class AlertParameters : CommonDialogParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[CommonDialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md) ← 
[AlertParameters](DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters.md)

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

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_AlertParameters_OkActionText"></a> OkActionText

Gets the localized text of the "OK" action.

```csharp
public string OkActionText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_AlertParameters_Url"></a> Url

Gets the URL of the web page that requested to display the dialog.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

