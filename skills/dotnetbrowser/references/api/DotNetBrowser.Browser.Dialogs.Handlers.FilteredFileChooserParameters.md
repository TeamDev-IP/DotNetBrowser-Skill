# <a id="DotNetBrowser_Browser_Dialogs_Handlers_FilteredFileChooserParameters"></a> Class FilteredFileChooserParameters

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for the common file chooser parameters.

```csharp
public abstract class FilteredFileChooserParameters : FileChooserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogParameters](DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md) ← 
[FileChooserParameters](DotNetBrowser.Browser.Dialogs.Handlers.FileChooserParameters.md) ← 
[FilteredFileChooserParameters](DotNetBrowser.Browser.Dialogs.Handlers.FilteredFileChooserParameters.md)

#### Derived

[OpenFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileParameters.md), 
[OpenMultipleFilesParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesParameters.md)

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

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_FilteredFileChooserParameters_AcceptableExtensions"></a> AcceptableExtensions

Gets the file extensions acceptable by the file chooser.

```csharp
public IEnumerable<string> AcceptableExtensions { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Remarks

The acceptable file extensions are based on the <code>accept</code> attribute value of the HTML input
element. The extensions do not include the preceding dot character.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_FilteredFileChooserParameters_FilterDescription"></a> FilterDescription

Gets the meaningful (e.g. "Image files", "PDF File (.pdf)",
etc.) description of the acceptable extensions.

```csharp
public string FilterDescription { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

