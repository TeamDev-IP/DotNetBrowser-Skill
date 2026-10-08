# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveAsPdfParameters"></a> Class SaveAsPdfParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SaveAsPdfHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveAsPdfParameters : FileChooserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[FileChooserParameters](DotNetBrowser.Browser.Dialogs.Handlers.FileChooserParameters.md) ← 
[SaveAsPdfParameters](DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfParameters.md)

#### Inherited Members

[DialogParameters.Browser](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md\#DotNetBrowser\_Browser\_Dialogs\_Handlers\_DialogParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveAsPdfParameters_SuggestedDirectory"></a> SuggestedDirectory

Gets the suggested directory where to save the PDF file.

```csharp
public string SuggestedDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveAsPdfParameters_SuggestedFileName"></a> SuggestedFileName

Gets the suggested name of the PDF file to save.

```csharp
public string SuggestedFileName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

