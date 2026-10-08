# <a id="DotNetBrowser_Ui_Bitmap"></a> Class Bitmap

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

Represents a binary image that consists of an image size and a byte array that contains the
pre-multiplied image pixels in the BGRA format.

```csharp
public sealed class Bitmap
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Bitmap](DotNetBrowser.Ui.Bitmap.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

#### Extension Methods

[BitmapExtensions.ToSkBitmap\(Bitmap\)](DotNetBrowser.AvaloniaUi.BitmapExtensions.md\#DotNetBrowser\_AvaloniaUi\_BitmapExtensions\_ToSkBitmap\_DotNetBrowser\_Ui\_Bitmap\_), 
[BitmapExtensions.ToSkImage\(Bitmap\)](DotNetBrowser.AvaloniaUi.BitmapExtensions.md\#DotNetBrowser\_AvaloniaUi\_BitmapExtensions\_ToSkImage\_DotNetBrowser\_Ui\_Bitmap\_), 
[BitmapExtensions.ToUiBitmap\(Bitmap, double\)](DotNetBrowser.AvaloniaUi.BitmapExtensions.md\#DotNetBrowser\_AvaloniaUi\_BitmapExtensions\_ToUiBitmap\_DotNetBrowser\_Ui\_Bitmap\_System\_Double\_)

## Properties

### <a id="DotNetBrowser_Ui_Bitmap_Pixels"></a> Pixels

Gets a read-only byte array that contains the pre-multiplied pixels of the binary image. Each pixel
allocates 4 bytes in the BGRA format.

```csharp
public IReadOnlyList<byte> Pixels { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[byte](https://learn.microsoft.com/dotnet/api/system.byte)\>

### <a id="DotNetBrowser_Ui_Bitmap_Size"></a> Size

Gets the size of this bitmap instance.

```csharp
public Size Size { get; }
```

#### Property Value

 [Size](DotNetBrowser.Geometry.Size.md)

