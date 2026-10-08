# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse"></a> Class SaveFileResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SaveFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class SaveFileResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SaveFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse_Canceled"></a> Canceled

Indicates whether the dialog was canceled.

```csharp
public bool Canceled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse_SelectedFile"></a> SelectedFile

Gets the selected file.

```csharp
public string SelectedFile { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the dialog was
canceled.

```csharp
public static SaveFileResponse Cancel()
```

#### Returns

 [SaveFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SaveFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse_SaveToFile_System_String_"></a> SaveToFile\(string\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the file was selected
in the file chooser
dialog.

```csharp
public static SaveFileResponse SaveToFile(string file)
```

#### Parameters

`file` [string](https://learn.microsoft.com/dotnet/api/system.string)

the selected file.

#### Returns

 [SaveFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SaveFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

