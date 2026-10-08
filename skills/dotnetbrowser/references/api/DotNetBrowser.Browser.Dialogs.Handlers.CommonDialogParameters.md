# <a id="DotNetBrowser_Browser_Dialogs_Handlers_CommonDialogParameters"></a> Class CommonDialogParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for common dialog parameters.

```csharp
public class CommonDialogParameters : DialogParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[CommonDialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md)

#### Derived

[AlertParameters](DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters.md), 
[BeforeUnloadParameters](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadParameters.md), 
[ConfirmParameters](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmParameters.md), 
[OpenExternalAppParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppParameters.md), 
[PromptParameters](DotNetBrowser.Browser.Dialogs.Handlers.PromptParameters.md), 
[RepostFormParameters](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormParameters.md), 
[SelectCertificateParameters](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.md)

#### Inherited Members

[DialogParameters.Browser](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_DialogParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_CommonDialogParameters_Message"></a> Message

Gets the localized dialog message.

```csharp
public string Message { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_CommonDialogParameters_Title"></a> Title

Gets the localized dialog title.

```csharp
public string Title { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

