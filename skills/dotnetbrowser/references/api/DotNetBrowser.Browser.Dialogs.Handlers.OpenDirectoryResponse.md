# <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse"></a> Class OpenDirectoryResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenDirectoryHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class OpenDirectoryResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenDirectoryResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse_Canceled"></a> Canceled

Indicates whether the dialog was canceled.

```csharp
public bool Canceled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse_SelectedDirectory"></a> SelectedDirectory

Gets the selected directory.

```csharp
public string SelectedDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the dialog was canceled.

```csharp
public static OpenDirectoryResponse Cancel()
```

#### Returns

 [OpenDirectoryResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenDirectoryHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse_SelectDirectory_System_String_"></a> SelectDirectory\(string\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the directory was selected in the
dialog.

```csharp
public static OpenDirectoryResponse SelectDirectory(string directory)
```

#### Parameters

`directory` [string](https://learn.microsoft.com/dotnet/api/system.string)

The selected directory.

#### Returns

 [OpenDirectoryResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenDirectoryHandler" data-throw-if-not-resolved="false"></xref> implementation.

