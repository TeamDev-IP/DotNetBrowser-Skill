# <a id="DotNetBrowser_Wpf_Dialogs_ColorExtensions"></a> Class ColorExtensions

Namespace: [DotNetBrowser.Wpf.Dialogs](DotNetBrowser.Wpf.Dialogs.md)  
Assembly: DotNetBrowser.Wpf.dll  

Extension methods for performing color conversion.

```csharp
public static class ColorExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ColorExtensions](DotNetBrowser.Wpf.Dialogs.ColorExtensions.md)

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Methods

### <a id="DotNetBrowser_Wpf_Dialogs_ColorExtensions_ToColor_DotNetBrowser_Ui_Color_"></a> ToColor\(Color\)

Converts the <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance to <xref href="System.Drawing.Color" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Color ToColor(this Color color)
```

#### Parameters

`color` Color

the color to convert

#### Returns

 [Color](https://learn.microsoft.com/dotnet/api/system.drawing.color)

the converted color.

### <a id="DotNetBrowser_Wpf_Dialogs_ColorExtensions_ToUIColor_System_Drawing_Color_"></a> ToUIColor\(Color\)

Converts the <xref href="System.Drawing.Color" data-throw-if-not-resolved="false"></xref> instance to <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Color ToUIColor(this Color color)
```

#### Parameters

`color` [Color](https://learn.microsoft.com/dotnet/api/system.drawing.color)

the color to convert

#### Returns

 Color

the converted color.

