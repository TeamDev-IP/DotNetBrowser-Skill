# <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse"></a> Class SelectColorResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SelectColorHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class SelectColorResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse_Cancelled"></a> Cancelled

Indicates whether the dialog was cancelled.

```csharp
public bool Cancelled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse_SelectedColor"></a> SelectedColor

Gets the selected color.

```csharp
public Color SelectedColor { get; }
```

#### Property Value

 [Color](DotNetBrowser.Ui.Color.md)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the user has cancelled color selection.

```csharp
public static SelectColorResponse Cancel()
```

#### Returns

 [SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SelectColorHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse_SelectColor_DotNetBrowser_Ui_Color_"></a> SelectColor\(Color\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the user has selected a color.

```csharp
public static SelectColorResponse SelectColor(Color color)
```

#### Parameters

`color` [Color](DotNetBrowser.Ui.Color.md)

The selected color.

#### Returns

 [SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SelectColorHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse_ShowDialog"></a> ShowDialog\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the default Chromium color picker
should be shown.

```csharp
public static SelectColorResponse ShowDialog()
```

#### Returns

 [SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.SelectColorHandler" data-throw-if-not-resolved="false"></xref> implementation.

