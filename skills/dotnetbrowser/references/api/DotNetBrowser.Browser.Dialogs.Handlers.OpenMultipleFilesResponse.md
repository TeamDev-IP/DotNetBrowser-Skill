# <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse"></a> Class OpenMultipleFilesResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenMultipleFilesHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenMultipleFilesResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenMultipleFilesResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse_Canceled"></a> Canceled

Indicates whether the dialog was canceled.

```csharp
public bool Canceled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse_SelectedFiles"></a> SelectedFiles

Gets the selected files.

```csharp
public IEnumerable<string> SelectedFiles { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the dialog was canceled.

```csharp
public static OpenMultipleFilesResponse Cancel()
```

#### Returns

 [OpenMultipleFilesResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenMultipleFilesHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse_SelectFiles_System_String___"></a> SelectFiles\(params string\[\]\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the files were selected in the
file chooser dialog.

```csharp
public static OpenMultipleFilesResponse SelectFiles(params string[] files)
```

#### Parameters

`files` [string](https://learn.microsoft.com/dotnet/api/system.string)\[\]

The selected files.

#### Returns

 [OpenMultipleFilesResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenMultipleFilesHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">files</code> collection is null, empty, contains null or
whitespace strings or contains strings that do not represent
the existing files.

