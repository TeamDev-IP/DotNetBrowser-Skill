# <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse"></a> Class OpenFileResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenFileResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse_Canceled"></a> Canceled

Indicates whether the dialog was canceled.

```csharp
public bool Canceled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse_SelectedFile"></a> SelectedFile

The selected file.

```csharp
public string SelectedFile { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse_Cancel"></a> Cancel\(\)

Creates an <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the dialog was canceled.

```csharp
public static OpenFileResponse Cancel()
```

#### Returns

 [OpenFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse_SelectFile_System_String_"></a> SelectFile\(string\)

Creates an <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the file was selected in the file chooser
dialog.

```csharp
public static OpenFileResponse SelectFile(string file)
```

#### Parameters

`file` [string](https://learn.microsoft.com/dotnet/api/system.string)

the selected file.

#### Returns

 [OpenFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

