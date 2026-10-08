# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters"></a> Class SaveFileParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SaveFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class SaveFileParameters : FileChooserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[FileChooserParameters](DotNetBrowser.Browser.Dialogs.Handlers.FileChooserParameters.md) ← 
[SaveFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileParameters.md)

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

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters_AcceptableExtensions"></a> AcceptableExtensions

Gets a list of the file extensions are based on the `accept` attribute value of the HTML input
element acceptable by the file chooser.

```csharp
public List<string> AcceptableExtensions { get; }
```

#### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters_FilterDescription"></a> FilterDescription

Gets a description of the acceptable extensions.

```csharp
public string FilterDescription { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters_IsAllFilesEnabled"></a> IsAllFilesEnabled

Indicates whether the file dialog should accept all files and show the "All files" filter.

```csharp
public bool IsAllFilesEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters_SuggestedDirectory"></a> SuggestedDirectory

Gets the suggested directory where to save the file.

```csharp
public string SuggestedDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters_SuggestedFileName"></a> SuggestedFileName

Gets the suggested name of the file to save.

```csharp
public string SuggestedFileName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

