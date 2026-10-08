# <a id="DotNetBrowser_Wpf_BitmapExtensions"></a> Class BitmapExtensions

Namespace: [DotNetBrowser.Wpf](DotNetBrowser.Wpf.md)  
Assembly: DotNetBrowser.Wpf.dll  

Extensions for <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> class.

```csharp
public static class BitmapExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BitmapExtensions](DotNetBrowser.Wpf.BitmapExtensions.md)

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Methods

### <a id="DotNetBrowser_Wpf_BitmapExtensions_ToBitmap_DotNetBrowser_Ui_Bitmap_"></a> ToBitmap\(Bitmap\)

Converts the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance to <xref href="System.Drawing.Bitmap" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Bitmap ToBitmap(this Bitmap bitmap)
```

#### Parameters

`bitmap` Bitmap

the bitmap to convert

#### Returns

 [Bitmap](https://learn.microsoft.com/dotnet/api/system.drawing.bitmap)

the converted bitmap.

### <a id="DotNetBrowser_Wpf_BitmapExtensions_ToBitmapSource_DotNetBrowser_Ui_Bitmap_"></a> ToBitmapSource\(Bitmap\)

Converts the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance to <xref href="System.Windows.Media.Imaging.BitmapSource" data-throw-if-not-resolved="false"></xref>
that can be then used in building the UI, e.g. displaying icons.

```csharp
public static BitmapSource ToBitmapSource(this Bitmap bitmap)
```

#### Parameters

`bitmap` Bitmap

the bitmap to convert

#### Returns

 [BitmapSource](https://learn.microsoft.com/dotnet/api/system.windows.media.imaging.bitmapsource)

the converted bitmap.

