# <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.AvaloniaUi.Dialogs](DotNetBrowser.AvaloniaUi.Dialogs.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md)

#### Derived

[DefaultAuthenticationHandler](DotNetBrowser.AvaloniaUi.Dialogs.DefaultAuthenticationHandler.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase__ctor_Avalonia_Visual_"></a> DialogHandlerBase\(Visual\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(Visual parent)
```

#### Parameters

`parent` Visual

The parent object for the dialog displayed by this handler.

## Properties

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner window for the
modal dialogs.

```csharp
public Visual Parent { get; }
```

#### Property Value

 Visual

## Methods

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase_FocusParent"></a> FocusParent\(\)

Tells the parent that it should request focus.

```csharp
protected void FocusParent()
```

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase_GetStorageProvider"></a> GetStorageProvider\(\)

Gets the <xref href="Avalonia.Platform.Storage.IStorageProvider" data-throw-if-not-resolved="false"></xref> that provides the file picker API.

```csharp
protected IStorageProvider GetStorageProvider()
```

#### Returns

 IStorageProvider

The <xref href="Avalonia.Platform.Storage.IStorageProvider" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DialogHandlerBase_UnfocusFocusBrowser_DotNetBrowser_Browser_IBrowser_"></a> UnfocusFocusBrowser\(IBrowser\)

Tells the Browser instance to unfocus and focus.
This method is used as a workaround because the default implementation of unfocus and focus
functionality (in the WindowedView class) does not give an expected keyboard focus result.

```csharp
protected void UnfocusFocusBrowser(IBrowser browser)
```

#### Parameters

`browser` [IBrowser](DotNetBrowser.Browser.IBrowser.md)

