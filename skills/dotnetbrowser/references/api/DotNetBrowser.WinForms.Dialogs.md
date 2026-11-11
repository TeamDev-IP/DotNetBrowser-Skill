# <a id="DotNetBrowser_WinForms_Dialogs"></a> Namespace DotNetBrowser.WinForms.Dialogs

### Classes

 [ColorExtensions](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_ColorExtensions)

Extension methods for performing color conversion.

 [DefaultAuthenticationHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler)

Default WinForms authentication handler, which displays an authentication dialog.

 [DefaultStartDownloadHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler)

The default WinForms implementation of <xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>, which displays a
save file
dialog to specify the path to store the downloaded file.

 [DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase)

The base class for all dialog handlers.

## <a id="DotNetBrowser_WinForms_Dialogs_ColorExtensions"></a> Class ColorExtensions

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

Extension methods for performing color conversion.

```csharp
public static class ColorExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ColorExtensions](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_ColorExtensions)

##### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

### Methods

#### <a id="DotNetBrowser_WinForms_Dialogs_ColorExtensions_ToColor_DotNetBrowser_Ui_Color_"></a> ToColor\(Color\)

Converts the <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance to <xref href="System.Drawing.Color" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Color ToColor(this Color color)
```

##### Parameters

`color` Color

the color to convert

##### Returns

 [Color](https://learn.microsoft.com/dotnet/api/system.drawing.color)

the converted color.

#### <a id="DotNetBrowser_WinForms_Dialogs_ColorExtensions_ToUIColor_System_Drawing_Color_"></a> ToUIColor\(Color\)

Converts the <xref href="System.Drawing.Color" data-throw-if-not-resolved="false"></xref> instance to <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Color ToUIColor(this Color color)
```

##### Parameters

`color` [Color](https://learn.microsoft.com/dotnet/api/system.drawing.color)

the color to convert

##### Returns

 Color

the converted color.

## <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler"></a> Class DefaultAuthenticationHandler

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

Default WinForms authentication handler, which displays an authentication dialog.

```csharp
public class DefaultAuthenticationHandler : DialogHandlerBase, IHandler<AuthenticateParameters, AuthenticateResponse>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase) ← 
[DefaultAuthenticationHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler)

##### Implements

IHandler<AuthenticateParameters, AuthenticateResponse\>

##### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase_Parent), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

### Constructors

#### <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler__ctor_System_Windows_Forms_Control_"></a> DefaultAuthenticationHandler\(Control\)

Creates and initializes the dialog handler.

```csharp
public DefaultAuthenticationHandler(Control parent)
```

##### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

### Methods

#### <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler_Handle_DotNetBrowser_Net_Handlers_AuthenticateParameters_"></a> Handle\(AuthenticateParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public AuthenticateResponse Handle(AuthenticateParameters parameters)
```

##### Parameters

`parameters` AuthenticateParameters

the handler parameters.

##### Returns

 AuthenticateResponse

an object that represents the response that should be
determined based on the provided parameters.

## <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler"></a> Class DefaultStartDownloadHandler

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

The default WinForms implementation of <xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>, which displays a
save file
dialog to specify the path to store the downloaded file.

```csharp
public class DefaultStartDownloadHandler : DialogHandlerBase, IHandler<StartDownloadParameters, StartDownloadResponse>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase) ← 
[DefaultStartDownloadHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler)

##### Implements

IHandler<StartDownloadParameters, StartDownloadResponse\>

##### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase_Parent), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

### Constructors

#### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler__ctor_System_Windows_Forms_Control_"></a> DefaultStartDownloadHandler\(Control\)

Creates and initializes the dialog handler.

```csharp
public DefaultStartDownloadHandler(Control parent)
```

##### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

### Properties

#### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler_InitialDirectory"></a> InitialDirectory

The initial directory that is displayed by the file dialog.

```csharp
public string InitialDirectory { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler_Handle_DotNetBrowser_Downloads_Handlers_StartDownloadParameters_"></a> Handle\(StartDownloadParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public StartDownloadResponse Handle(StartDownloadParameters startDownloadParameters)
```

##### Parameters

`startDownloadParameters` StartDownloadParameters

the item for which the download is about to be started.

##### Returns

 StartDownloadResponse

an object that represents the response that should be
determined based on the provided parameters.

## <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DialogHandlerBase)

##### Derived

[DefaultAuthenticationHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler), 
[DefaultStartDownloadHandler](DotNetBrowser.WinForms.Dialogs.md#DotNetBrowser_WinForms_Dialogs_DefaultStartDownloadHandler)

##### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

### Constructors

#### <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase__ctor_System_Windows_Forms_Control_"></a> DialogHandlerBase\(Control\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(Control parent)
```

##### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

### Properties

#### <a id="DotNetBrowser_WinForms_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner window for the
modal dialogs.

```csharp
public Control Parent { get; }
```

##### Property Value

 [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)
