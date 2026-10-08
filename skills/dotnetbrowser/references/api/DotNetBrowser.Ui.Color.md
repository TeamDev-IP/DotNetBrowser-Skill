# <a id="DotNetBrowser_Ui_Color"></a> Class Color

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

A numeric model of an RGB color. The components of the color instance are presented in the
arithmetic notation. This means that each component accepts any fractional value from 0 to 1.

```csharp
public sealed class Color : IFormattable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Color](DotNetBrowser.Ui.Color.md)

#### Implements

[IFormattable](https://learn.microsoft.com/dotnet/api/system.iformattable)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
    If all the components except <code>alpha</code> are at zero and the <code>alpha</code> is at 1, the
    result is black. If all are at 1, the result is the brightest representable white.
</p>
<p>
    <b>Important:</b>  the component values out of the <code>0..1</code> range are not allowed and
    should not be used.
</p>

## Constructors

### <a id="DotNetBrowser_Ui_Color__ctor_System_Single_System_Single_System_Single_System_Single_"></a> Color\(float, float, float, float\)

Initializes a new <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance with the specified channel values.

```csharp
public Color(float red, float green, float blue, float alpha = 1)
```

#### Parameters

`red` [float](https://learn.microsoft.com/dotnet/api/system.single)

The red channel value.

`green` [float](https://learn.microsoft.com/dotnet/api/system.single)

The green channel value.

`blue` [float](https://learn.microsoft.com/dotnet/api/system.single)

The blue channel value.

`alpha` [float](https://learn.microsoft.com/dotnet/api/system.single)

The alpha channel value.

#### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

thrown when any of the parameters is outside the <code>0..1</code> range.

## Properties

### <a id="DotNetBrowser_Ui_Color_Alpha"></a> Alpha

Gets the opacity channel value in the <code>0..1</code> range. When the value is 1, the color
is 100% opaque. When 0, the color is 100% transparent.

```csharp
public float Alpha { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Ui_Color_Blue"></a> Blue

Gets the blue channel value in the <code>0..1</code> range.

```csharp
public float Blue { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Ui_Color_Green"></a> Green

Gets the green channel value in the <code>0..1</code> range.

```csharp
public float Green { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Ui_Color_Red"></a> Red

Gets the red channel value in the <code>0..1</code> range.

```csharp
public float Red { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

## Methods

### <a id="DotNetBrowser_Ui_Color_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Ui_Color_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Ui_Color_ToHexRGB"></a> ToHexRGB\(\)

Creates a string representation for this color in the <code>RGB</code> hex format.

```csharp
public string ToHexRGB()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation for this color in the <code>RGB</code> hex format.

### <a id="DotNetBrowser_Ui_Color_ToHexRGBA"></a> ToHexRGBA\(\)

Creates a string representation for this color in the <code>RGBA</code> hex format.

```csharp
public string ToHexRGBA()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation for this color in the <code>RGBA</code> hex format.

### <a id="DotNetBrowser_Ui_Color_ToString_System_String_System_IFormatProvider_"></a> ToString\(string, IFormatProvider\)

```csharp
public string ToString(string format, IFormatProvider formatProvider)
```

#### Parameters

`format` [string](https://learn.microsoft.com/dotnet/api/system.string)

`formatProvider` [IFormatProvider](https://learn.microsoft.com/dotnet/api/system.iformatprovider)

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>The supported format strings are:</p>
<ul><li><span class="term">G</span>
            General string representation:
            <code>Red: &lt;value&gt;, Green: &lt;value&gt;, Blue: &lt;value&gt;, Alpha: &lt;value&gt;</code>
        </li><li><span class="term">RGB</span>Hexademical representation (with alpha omitted): <code>RRGGBB</code>.</li><li><span class="term">RGBA</span>Hexademical representation: <code>RRGGBBAA</code>.</li></ul>

### <a id="DotNetBrowser_Ui_Color_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Ui_Color_ToString_System_String_"></a> ToString\(string\)

Returns a string representation of the value of this <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref> instance, according to the provided
format specifier.

```csharp
public string ToString(string format)
```

#### Parameters

`format` [string](https://learn.microsoft.com/dotnet/api/system.string)

A single format specifier that indicates how to format the value of this Color. The format
parameter can be "G", "F", "RGB", or "RGBA". If format is null or an empty string (""), "G" is used.

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The value of this <xref href="DotNetBrowser.Ui.Color" data-throw-if-not-resolved="false"></xref>, represented  in the specified format.

#### Remarks

<p>The supported format strings are:</p>
<ul><li><span class="term">G</span>
            General string representation:
            <code>Red: &lt;value&gt;, Green: &lt;value&gt;, Blue: &lt;value&gt;, Alpha: &lt;value&gt;</code>
        </li><li><span class="term">RGB</span>Hexademical representation (with alpha omitted): <code>RRGGBB</code>.</li><li><span class="term">RGBA</span>Hexademical representation: <code>RRGGBBAA</code>.</li></ul>

