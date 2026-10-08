# <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppParameters"></a> Class OpenExternalAppParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenExternalAppHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExternalAppParameters : CommonDialogParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[CommonDialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md) ← 
[OpenExternalAppParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppParameters.md)

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

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppParameters_CancelActionText"></a> CancelActionText

Gets the localized text of the "Cancel" action.

```csharp
public string CancelActionText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppParameters_OpenActionText"></a> OpenActionText

Gets the localized text of the "Open..." action.

```csharp
public string OpenActionText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppParameters_Url"></a> Url

Gets the URL of the external application request that is about to be opened.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

