# <a id="DotNetBrowser_WinUi3_BitmapExtensions"></a> Class BitmapExtensions

Namespace: [DotNetBrowser.WinUi3](DotNetBrowser.WinUi3.md)  
Assembly: DotNetBrowser.WinUi3.dll  

Extensions for <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> class.

```csharp
public static class BitmapExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BitmapExtensions](DotNetBrowser.WinUi3.BitmapExtensions.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_WinUi3_BitmapExtensions_ToBitmap_DotNetBrowser_Ui_Bitmap_"></a> ToBitmap\(Bitmap\)

Converts the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance to <xref href="Windows.Graphics.Imaging.SoftwareBitmap" data-throw-if-not-resolved="false"></xref>.

```csharp
public static SoftwareBitmap ToBitmap(this Bitmap bitmap)
```

#### Parameters

`bitmap` Bitmap

the bitmap to convert

#### Returns

 [SoftwareBitmap](https://learn.microsoft.com/uwp/api/windows.graphics.imaging.softwarebitmap)

the converted bitmap.

### <a id="DotNetBrowser_WinUi3_BitmapExtensions_ToBitmapSourceAsync_DotNetBrowser_Ui_Bitmap_"></a> ToBitmapSourceAsync\(Bitmap\)

Converts the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance to <xref href="Microsoft.UI.Xaml.Media.Imaging.SoftwareBitmapSource" data-throw-if-not-resolved="false"></xref>
that can be then used in building the UI, e.g., displaying icons.

```csharp
public static Task<SoftwareBitmapSource> ToBitmapSourceAsync(this Bitmap bitmap)
```

#### Parameters

`bitmap` Bitmap

the bitmap to convert

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[SoftwareBitmapSource](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.media.imaging.softwarebitmapsource)\>

the converted bitmap.

