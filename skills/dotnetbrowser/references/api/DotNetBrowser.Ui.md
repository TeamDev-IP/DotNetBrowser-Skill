# <a id="DotNetBrowser_Ui"></a> Namespace DotNetBrowser.Ui

### Namespaces

 [DotNetBrowser.Ui.Cursors](DotNetBrowser.Ui.Cursors.md)

### Classes

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

Represents a binary image that consists of an image size and a byte array that contains the
pre-multiplied image pixels in the BGRA format.

 [Color](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Color)

A numeric model of an RGB color. The components of the color instance are presented in the
arithmetic notation. This means that each component accepts any fractional value from 0 to 1.

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

A system font.

 [FontSize](DotNetBrowser.Ui.md#DotNetBrowser_Ui_FontSize)

The browser font size.

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

The supported user interface languages.

## <a id="DotNetBrowser_Ui_Bitmap"></a> Class Bitmap

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

Represents a binary image that consists of an image size and a byte array that contains the
pre-multiplied image pixels in the BGRA format.

```csharp
public sealed class Bitmap
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

##### Extension Methods

[BitmapExtensions.ToSkBitmap\(Bitmap\)](DotNetBrowser.AvaloniaUi.md#DotNetBrowser_AvaloniaUi_BitmapExtensions_ToSkBitmap_DotNetBrowser_Ui_Bitmap_), 
[BitmapExtensions.ToSkImage\(Bitmap\)](DotNetBrowser.AvaloniaUi.md#DotNetBrowser_AvaloniaUi_BitmapExtensions_ToSkImage_DotNetBrowser_Ui_Bitmap_), 
[BitmapExtensions.ToUiBitmap\(Bitmap, double\)](DotNetBrowser.AvaloniaUi.md#DotNetBrowser_AvaloniaUi_BitmapExtensions_ToUiBitmap_DotNetBrowser_Ui_Bitmap_System_Double_)

### Properties

#### <a id="DotNetBrowser_Ui_Bitmap_Pixels"></a> Pixels

Gets a read-only byte array that contains the pre-multiplied pixels of the binary image. Each pixel
allocates 4 bytes in the BGRA format.

```csharp
public IReadOnlyList<byte> Pixels { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[byte](https://learn.microsoft.com/dotnet/api/system.byte)\>

#### <a id="DotNetBrowser_Ui_Bitmap_Size"></a> Size

Gets the size of this bitmap instance.

```csharp
public Size Size { get; }
```

##### Property Value

 [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

## <a id="DotNetBrowser_Ui_Color"></a> Class Color

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

A numeric model of an RGB color. The components of the color instance are presented in the
arithmetic notation. This means that each component accepts any fractional value from 0 to 1.

```csharp
public sealed class Color : IFormattable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Color](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Color)

##### Implements

[IFormattable](https://learn.microsoft.com/dotnet/api/system.iformattable)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    If all the components except <code>alpha</code> are at zero and the <code>alpha</code> is at 1, the
    result is black. If all are at 1, the result is the brightest representable white.
</p>
<p>
    <b>Important:</b>  the component values out of the <code>0..1</code> range are not allowed and
    should not be used.
</p>

### Constructors

#### <a id="DotNetBrowser_Ui_Color__ctor_System_Single_System_Single_System_Single_System_Single_"></a> Color\(float, float, float, float\)

Initializes a new <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance with the specified channel values.

```csharp
public Color(float red, float green, float blue, float alpha = 1)
```

##### Parameters

`red` [float](https://learn.microsoft.com/dotnet/api/system.single)

The red channel value.

`green` [float](https://learn.microsoft.com/dotnet/api/system.single)

The green channel value.

`blue` [float](https://learn.microsoft.com/dotnet/api/system.single)

The blue channel value.

`alpha` [float](https://learn.microsoft.com/dotnet/api/system.single)

The alpha channel value.

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

thrown when any of the parameters is outside the <code>0..1</code> range.

### Properties

#### <a id="DotNetBrowser_Ui_Color_Alpha"></a> Alpha

Gets the opacity channel value in the <code>0..1</code> range. When the value is 1, the color
is 100% opaque. When 0, the color is 100% transparent.

```csharp
public float Alpha { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Ui_Color_Blue"></a> Blue

Gets the blue channel value in the <code>0..1</code> range.

```csharp
public float Blue { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Ui_Color_Green"></a> Green

Gets the green channel value in the <code>0..1</code> range.

```csharp
public float Green { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Ui_Color_Red"></a> Red

Gets the red channel value in the <code>0..1</code> range.

```csharp
public float Red { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### Methods

#### <a id="DotNetBrowser_Ui_Color_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Ui_Color_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Ui_Color_ToHexRGB"></a> ToHexRGB\(\)

Creates a string representation for this color in the <code>RGB</code> hex format.

```csharp
public string ToHexRGB()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation for this color in the <code>RGB</code> hex format.

#### <a id="DotNetBrowser_Ui_Color_ToHexRGBA"></a> ToHexRGBA\(\)

Creates a string representation for this color in the <code>RGBA</code> hex format.

```csharp
public string ToHexRGBA()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation for this color in the <code>RGBA</code> hex format.

#### <a id="DotNetBrowser_Ui_Color_ToString_System_String_System_IFormatProvider_"></a> ToString\(string, IFormatProvider\)

```csharp
public string ToString(string format, IFormatProvider formatProvider)
```

##### Parameters

`format` [string](https://learn.microsoft.com/dotnet/api/system.string)

`formatProvider` [IFormatProvider](https://learn.microsoft.com/dotnet/api/system.iformatprovider)

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>The supported format strings are:</p>
<ul><li><span class="term">G</span>
            General string representation:
            <code>Red: &lt;value&gt;, Green: &lt;value&gt;, Blue: &lt;value&gt;, Alpha: &lt;value&gt;</code>
        </li><li><span class="term">RGB</span>Hexademical representation (with alpha omitted): <code>RRGGBB</code>.</li><li><span class="term">RGBA</span>Hexademical representation: <code>RRGGBBAA</code>.</li></ul>

#### <a id="DotNetBrowser_Ui_Color_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Ui_Color_ToString_System_String_"></a> ToString\(string\)

Returns a string representation of the value of this <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance, according to the provided
format specifier.

```csharp
public string ToString(string format)
```

##### Parameters

`format` [string](https://learn.microsoft.com/dotnet/api/system.string)

A single format specifier that indicates how to format the value of this Color. The format
parameter can be "G", "F", "RGB", or "RGBA". If format is null or an empty string (""), "G" is used.

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The value of this <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref>, represented  in the specified format.

##### Remarks

<p>The supported format strings are:</p>
<ul><li><span class="term">G</span>
            General string representation:
            <code>Red: &lt;value&gt;, Green: &lt;value&gt;, Blue: &lt;value&gt;, Alpha: &lt;value&gt;</code>
        </li><li><span class="term">RGB</span>Hexademical representation (with alpha omitted): <code>RRGGBB</code>.</li><li><span class="term">RGBA</span>Hexademical representation: <code>RRGGBBAA</code>.</li></ul>

## <a id="DotNetBrowser_Ui_Font"></a> Class Font

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

A system font.

```csharp
public sealed class Font
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Ui_Font_DisplayName"></a> DisplayName

Gets the human-readable name of the font.

```csharp
public string DisplayName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Ui_Font_Name"></a> Name

Gets the internal name of the font.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Ui_Font_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Ui_Font_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Ui_FontSize"></a> Class FontSize

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

The browser font size.

```csharp
public sealed class FontSize
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FontSize](DotNetBrowser.Ui.md#DotNetBrowser_Ui_FontSize)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Ui_FontSize__ctor_System_Int32_"></a> FontSize\(int\)

Creates a new font size.

```csharp
public FontSize(int value)
```

##### Parameters

`value` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The font size in pixels. Cannot be zero or negative.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The font size in pixels is zero or negative.

### Properties

#### <a id="DotNetBrowser_Ui_FontSize_Value"></a> Value

Gets the font size in pixels.

```csharp
public int Value { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Ui_FontSize_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Ui_FontSize_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Operators

#### <a id="DotNetBrowser_Ui_FontSize_op_Implicit_DotNetBrowser_Ui_FontSize__System_Int32"></a> implicit operator int\(FontSize\)

Converts the font size to integer.

```csharp
public static implicit operator int(FontSize size)
```

##### Parameters

`size` [FontSize](DotNetBrowser.Ui.md#DotNetBrowser_Ui_FontSize)

The font size to convert.

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Ui_FontSize_op_Implicit_System_Int32__DotNetBrowser_Ui_FontSize"></a> implicit operator FontSize\(int\)

Converts an integer to the font size.

```csharp
public static implicit operator FontSize(int value)
```

##### Parameters

`value` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The font size in pixels. Cannot be zero or negative.

##### Returns

 [FontSize](DotNetBrowser.Ui.md#DotNetBrowser_Ui_FontSize)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The font size in pixels is zero or negative.

## <a id="DotNetBrowser_Ui_Language"></a> Class Language

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

The supported user interface languages.

```csharp
public sealed class Language : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Ui_Language_Amharic"></a> Amharic

Amharic language ("am")

```csharp
public static readonly Language Amharic
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Arabic"></a> Arabic

Arabic language ("ar")

```csharp
public static readonly Language Arabic
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Bengali"></a> Bengali

Bengali language ("bn")

```csharp
public static readonly Language Bengali
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Bulgarian"></a> Bulgarian

Bulgarian language ("bg")

```csharp
public static readonly Language Bulgarian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Catalan"></a> Catalan

Catalan language ("ca")

```csharp
public static readonly Language Catalan
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Chinese"></a> Chinese

Chinese language ("zh-cn")

```csharp
public static readonly Language Chinese
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_ChineseTaiwan"></a> ChineseTaiwan

Chinese (Taiwan) language ("zh-tw")

```csharp
public static readonly Language ChineseTaiwan
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Czech"></a> Czech

Czech language ("cs")

```csharp
public static readonly Language Czech
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Danish"></a> Danish

Danish language ("da")

```csharp
public static readonly Language Danish
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Default"></a> Default

Default language (English).

```csharp
public static readonly Language Default
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Dutch"></a> Dutch

Dutch language ("nl")

```csharp
public static readonly Language Dutch
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_EnglishUk"></a> EnglishUk

English (UK) language ("en-gb")

```csharp
public static readonly Language EnglishUk
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_EnglishUs"></a> EnglishUs

English (US) language ("en-us")

```csharp
public static readonly Language EnglishUs
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Estonian"></a> Estonian

Estonian language ("et")

```csharp
public static readonly Language Estonian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Filipino"></a> Filipino

Filipino language ("fil")

```csharp
public static readonly Language Filipino
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Finnish"></a> Finnish

Finnish language ("fi")

```csharp
public static readonly Language Finnish
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_French"></a> French

French (France) language ("fr")

```csharp
public static readonly Language French
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_German"></a> German

German language ("de")

```csharp
public static readonly Language German
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Greek"></a> Greek

Greek language ("el")

```csharp
public static readonly Language Greek
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Gujarati"></a> Gujarati

Gujarati language ("gu")

```csharp
public static readonly Language Gujarati
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Hebrew"></a> Hebrew

Hebrew language ("he")

```csharp
public static readonly Language Hebrew
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Hindi"></a> Hindi

Hindi language ("hi")

```csharp
public static readonly Language Hindi
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Hungarian"></a> Hungarian

Hungarian language ("hu")

```csharp
public static readonly Language Hungarian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Indonesian"></a> Indonesian

Indonesian language ("id")

```csharp
public static readonly Language Indonesian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Italian"></a> Italian

Italian language ("it")

```csharp
public static readonly Language Italian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Japanese"></a> Japanese

Japanese language ("ja")

```csharp
public static readonly Language Japanese
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Kannada"></a> Kannada

Kannada language ("kn")

```csharp
public static readonly Language Kannada
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Korean"></a> Korean

Korean language ("ko")

```csharp
public static readonly Language Korean
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Latvian"></a> Latvian

Latvian language ("lv")

```csharp
public static readonly Language Latvian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Lithuanian"></a> Lithuanian

Lithuanian language ("lt")

```csharp
public static readonly Language Lithuanian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Malay"></a> Malay

Malay language ("ms")

```csharp
public static readonly Language Malay
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Malayalam"></a> Malayalam

Malayalam language ("ml")

```csharp
public static readonly Language Malayalam
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Marathi"></a> Marathi

Marathi language ("mr")

```csharp
public static readonly Language Marathi
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Norwegian"></a> Norwegian

Norwegian language ("nb")

```csharp
public static readonly Language Norwegian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Persian"></a> Persian

Persian language ("fa")

```csharp
public static readonly Language Persian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Polish"></a> Polish

Polish language ("pl")

```csharp
public static readonly Language Polish
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_PortugueseBrazil"></a> PortugueseBrazil

Portuguese (Brazil) language ("pt-br")

```csharp
public static readonly Language PortugueseBrazil
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_PortuguesePortugal"></a> PortuguesePortugal

Portuguese (Portugal) language ("pt-pt")

```csharp
public static readonly Language PortuguesePortugal
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Romanian"></a> Romanian

Romanian language ("ro")

```csharp
public static readonly Language Romanian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Russian"></a> Russian

Russian language ("ru")

```csharp
public static readonly Language Russian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Serbian"></a> Serbian

Serbian language ("sr")

```csharp
public static readonly Language Serbian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Slovak"></a> Slovak

Slovak language ("sk")

```csharp
public static readonly Language Slovak
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Slovenian"></a> Slovenian

Slovenian language ("sl")

```csharp
public static readonly Language Slovenian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_SpanishLatinAmerica"></a> SpanishLatinAmerica

Spanish (Latin America) language ("es-419")

```csharp
public static readonly Language SpanishLatinAmerica
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_SpanishSpain"></a> SpanishSpain

Spanish language (Spain) ("es")

```csharp
public static readonly Language SpanishSpain
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Swahili"></a> Swahili

Swahili language ("sw")

```csharp
public static readonly Language Swahili
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Swedish"></a> Swedish

Swedish language ("sv")

```csharp
public static readonly Language Swedish
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Tamil"></a> Tamil

Tamil language ("ta")

```csharp
public static readonly Language Tamil
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Telugu"></a> Telugu

Telugu language ("te")

```csharp
public static readonly Language Telugu
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Thai"></a> Thai

Thai language ("th")

```csharp
public static readonly Language Thai
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Turkish"></a> Turkish

Turkish language ("tr")

```csharp
public static readonly Language Turkish
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Ukrainian"></a> Ukrainian

Ukrainian language ("uk")

```csharp
public static readonly Language Ukrainian
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

#### <a id="DotNetBrowser_Ui_Language_Vietnamese"></a> Vietnamese

Vietnamese language ("vi")

```csharp
public static readonly Language Vietnamese
```

##### Field Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

### Methods

#### <a id="DotNetBrowser_Ui_Language_FromCulture_System_Globalization_CultureInfo_"></a> FromCulture\(CultureInfo\)

Initializes the <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance from the specified culture information.

```csharp
public static Language FromCulture(CultureInfo cultureInfo)
```

##### Parameters

`cultureInfo` [CultureInfo](https://learn.microsoft.com/dotnet/api/system.globalization.cultureinfo)

The culture information.

##### Returns

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

The <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Ui_Language_FromString_System_String_"></a> FromString\(string\)

Returns the <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static Language FromString(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language string representation

##### Returns

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

The <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.

### Operators

#### <a id="DotNetBrowser_Ui_Language_op_Explicit_System_Globalization_CultureInfo__DotNetBrowser_Ui_Language"></a> explicit operator Language\(CultureInfo\)

Returns the <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance by the specified culture information.

```csharp
public static explicit operator Language(CultureInfo cultureInfo)
```

##### Parameters

`cultureInfo` [CultureInfo](https://learn.microsoft.com/dotnet/api/system.globalization.cultureinfo)

The culture information.

##### Returns

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

The <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the specified culture information.

#### <a id="DotNetBrowser_Ui_Language_op_Explicit_System_String__DotNetBrowser_Ui_Language"></a> explicit operator Language\(string\)

Returns the <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static explicit operator Language(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language string representation

##### Returns

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

The <xref href="DotNetBrowser.Ui.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.
