# <a id="DotNetBrowser_AvaloniaUi_BitmapExtensions"></a> Class BitmapExtensions

Namespace: [DotNetBrowser.AvaloniaUi](DotNetBrowser.AvaloniaUi.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

Extensions for <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> class.

```csharp
public static class BitmapExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BitmapExtensions](DotNetBrowser.AvaloniaUi.BitmapExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_AvaloniaUi_BitmapExtensions_ToSkBitmap_DotNetBrowser_Ui_Bitmap_"></a> ToSkBitmap\(Bitmap\)

Converts a <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> to the SkiaSharp <xref href="SkiaSharp.SKBitmap" data-throw-if-not-resolved="false"></xref>.

```csharp
public static SKBitmap ToSkBitmap(this Bitmap bitmap)
```

#### Parameters

`bitmap` [Bitmap](DotNetBrowser.Ui.Bitmap.md)

The bitmap to convert.

#### Returns

 [SKBitmap](https://learn.microsoft.com/dotnet/api/skiasharp.skbitmap)

The converted <xref href="SkiaSharp.SKBitmap" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_AvaloniaUi_BitmapExtensions_ToSkImage_DotNetBrowser_Ui_Bitmap_"></a> ToSkImage\(Bitmap\)

Converts a <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> to the SkiaSharp <xref href="SkiaSharp.SKImage" data-throw-if-not-resolved="false"></xref>.

```csharp
public static SKImage ToSkImage(this Bitmap bitmap)
```

#### Parameters

`bitmap` [Bitmap](DotNetBrowser.Ui.Bitmap.md)

The bitmap to convert.

#### Returns

 [SKImage](https://learn.microsoft.com/dotnet/api/skiasharp.skimage)

The converted <xref href="SkiaSharp.SKImage" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_AvaloniaUi_BitmapExtensions_ToUiBitmap_DotNetBrowser_Ui_Bitmap_System_Double_"></a> ToUiBitmap\(Bitmap, double\)

Converts a <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> to the Avalonia UI <xref href="Avalonia.Media.Imaging.IBitmap" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Bitmap ToUiBitmap(this Bitmap bitmap, double scaleFactor = 1)
```

#### Parameters

`bitmap` [Bitmap](DotNetBrowser.Ui.Bitmap.md)

The bitmap to convert.

`scaleFactor` [double](https://learn.microsoft.com/dotnet/api/system.double)

#### Returns

 Bitmap

The converted <xref href="Avalonia.Media.Imaging.IBitmap" data-throw-if-not-resolved="false"></xref> instance.

