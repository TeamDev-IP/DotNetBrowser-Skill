# <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler"></a> Class DefaultStartDownloadHandler

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

The default WinForms implementation of <xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>, which displays a
save file
dialog to specify the path to store the downloaded file.

```csharp
public class DefaultStartDownloadHandler : DialogHandlerBase, IHandler<StartDownloadParameters, StartDownloadResponse>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md) ← 
[DefaultStartDownloadHandler](DotNetBrowser.WinForms.Dialogs.DefaultStartDownloadHandler.md)

#### Implements

IHandler<StartDownloadParameters, StartDownloadResponse\>

#### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_WinForms\_Dialogs\_DialogHandlerBase\_Parent), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Constructors

### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler__ctor_System_Windows_Forms_Control_"></a> DefaultStartDownloadHandler\(Control\)

Creates and initializes the dialog handler.

```csharp
public DefaultStartDownloadHandler(Control parent)
```

#### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

## Properties

### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler_InitialDirectory"></a> InitialDirectory

The initial directory that is displayed by the file dialog.

```csharp
public string InitialDirectory { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler_Handle_DotNetBrowser_Downloads_Handlers_StartDownloadParameters_"></a> Handle\(StartDownloadParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public StartDownloadResponse Handle(StartDownloadParameters startDownloadParameters)
```

#### Parameters

`startDownloadParameters` StartDownloadParameters

the item for which the download is about to be started.

#### Returns

 StartDownloadResponse

an object that represents the response that should be
determined based on the provided parameters.

