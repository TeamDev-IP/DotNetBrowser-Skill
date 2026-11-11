# <a id="DotNetBrowser_Geometry"></a> Namespace DotNetBrowser.Geometry

### Classes

 [Ellipse](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Ellipse)

Represents a three numbers that are used to define ellipse size and orientation in the
two-dimensional space.

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

Represents a pair of numbers that in general are used to define coordinates in the
two-dimensional space.

 [Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

Represents a rectangle described by the location and dimensions.

 [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

Represents a pair of numbers that in general are used to define dimensions in the
two-dimensional space.

## <a id="DotNetBrowser_Geometry_Ellipse"></a> Class Ellipse

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a three numbers that are used to define ellipse size and orientation in the
two-dimensional space.

```csharp
public sealed class Ellipse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Ellipse](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Ellipse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Geometry_Ellipse__ctor_System_Single_System_Single_System_Single_"></a> Ellipse\(float, float, float\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Ellipse" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">radiusX</code> and
<code class="paramref">radiusY</code> radii.

```csharp
public Ellipse(float radiusX, float radiusY, float rotationAngle = 0)
```

##### Parameters

`radiusX` [float](https://learn.microsoft.com/dotnet/api/system.single)

Radius X axis size.

`radiusY` [float](https://learn.microsoft.com/dotnet/api/system.single)

Radius X axis size.

`rotationAngle` [float](https://learn.microsoft.com/dotnet/api/system.single)

Ellipse orientation angle.

### Properties

#### <a id="DotNetBrowser_Geometry_Ellipse_RadiusX"></a> RadiusX

Gets radius X axis length.

```csharp
public float RadiusX { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Geometry_Ellipse_RadiusY"></a> RadiusY

Gets radius Y axis length.

```csharp
public float RadiusY { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Geometry_Ellipse_RotationAngle"></a> RotationAngle

Gets ellipse orientation angle.

```csharp
public float RotationAngle { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### Methods

#### <a id="DotNetBrowser_Geometry_Ellipse_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Ellipse_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Geometry_Point"></a> Class Point

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a pair of numbers that in general are used to define coordinates in the
two-dimensional space.

```csharp
public sealed class Point
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Geometry_Point__ctor_System_Int32_System_Int32_"></a> Point\(int, int\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Point" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">x</code> and
<code class="paramref">y</code> coordinates.

```csharp
public Point(int x, int y)
```

##### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The horizontal coordinate.

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The vertical coordinate.

### Fields

#### <a id="DotNetBrowser_Geometry_Point_Empty"></a> Empty

An empty <code>Point</code> that has x and y values set to zero.

```csharp
public static readonly Point Empty
```

##### Field Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

### Properties

#### <a id="DotNetBrowser_Geometry_Point_X"></a> X

Gets the horizontal coordinate.

```csharp
public int X { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Geometry_Point_Y"></a> Y

Gets the vertical coordinate.

```csharp
public int Y { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Geometry_Point_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Point_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Geometry_Point_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Geometry_Rectangle"></a> Class Rectangle

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a rectangle described by the location and dimensions.

```csharp
public sealed class Rectangle
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Geometry_Rectangle__ctor_DotNetBrowser_Geometry_Point_DotNetBrowser_Geometry_Size_"></a> Rectangle\(Point, Size\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">origin</code> and
<code class="paramref">size</code>.

```csharp
public Rectangle(Point origin, Size size)
```

##### Parameters

`origin` [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

The top-left corner coordinate of the rectangle.

`size` [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

The rectangle dimensions.

#### <a id="DotNetBrowser_Geometry_Rectangle__ctor_System_Int32_System_Int32_System_UInt32_System_UInt32_"></a> Rectangle\(int, int, uint, uint\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> class with the specified parameters.

```csharp
public Rectangle(int x, int y, uint width, uint height)
```

##### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The top-left corner X coordinate of the rectangle.

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The top-left corner Y coordinate of the rectangle.

`width` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The rectangle width.

`height` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The rectangle height.

### Properties

#### <a id="DotNetBrowser_Geometry_Rectangle_IsEmpty"></a> IsEmpty

Indicates whether all numeric properties of this Rectangle have values of zero.

```csharp
public bool IsEmpty { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Rectangle_Origin"></a> Origin

Gets the top-left corner coordinate of the rectangle.

```csharp
public Point Origin { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Geometry_Rectangle_Size"></a> Size

Gets the rectangle dimensions.

```csharp
public Size Size { get; }
```

##### Property Value

 [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

### Methods

#### <a id="DotNetBrowser_Geometry_Rectangle_Center"></a> Center\(\)

Calculates the center of this rectangle.

```csharp
public Point Center()
```

##### Returns

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

The point that represents the center of this rectangle.

#### <a id="DotNetBrowser_Geometry_Rectangle_Contains_DotNetBrowser_Geometry_Point_"></a> Contains\(Point\)

Checks whether the rectangle contains the specified point.

```csharp
public bool Contains(Point point)
```

##### Parameters

`point` [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

the <xref href="DotNetBrowser.Geometry.Point" data-throw-if-not-resolved="false"></xref> instance to check.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the rectangle contains this point; false otherwise.

#### <a id="DotNetBrowser_Geometry_Rectangle_Contains_DotNetBrowser_Geometry_Rectangle_"></a> Contains\(Rectangle\)

Checks whether the rectangle contains the specified rectangle.

```csharp
public bool Contains(Rectangle other)
```

##### Parameters

`other` [Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> instance to check.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the rectangle contains the other rectangle; false otherwise.

#### <a id="DotNetBrowser_Geometry_Rectangle_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Rectangle_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Geometry_Rectangle_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Geometry_Size"></a> Class Size

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a pair of numbers that in general are used to define dimensions in the
two-dimensional space.

```csharp
public class Size
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Geometry_Size__ctor_System_UInt32_System_UInt32_"></a> Size\(uint, uint\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Size" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">width</code> and
<code class="paramref">height</code>.

```csharp
public Size(uint width, uint height)
```

##### Parameters

`width` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

the horizontal dimension. Cannot be negative.

`height` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

the vertical dimension. Cannot be negative.

### Fields

#### <a id="DotNetBrowser_Geometry_Size_Empty"></a> Empty

An empty <code>Size</code> that has x and y values set to zero.

```csharp
public static readonly Size Empty
```

##### Field Value

 [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

### Properties

#### <a id="DotNetBrowser_Geometry_Size_Height"></a> Height

Gets the vertical dimension.

```csharp
public uint Height { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### <a id="DotNetBrowser_Geometry_Size_IsEmpty"></a> IsEmpty

Indicates whether width and height of this Size have values of zero.

```csharp
public bool IsEmpty { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Size_Width"></a> Width

Gets the horizontal dimension.

```csharp
public uint Width { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### Methods

#### <a id="DotNetBrowser_Geometry_Size_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Geometry_Size_Equals_DotNetBrowser_Geometry_Size_"></a> Equals\(Size\)

Determines whether the specified <code>Size</code> object is equal to the current object.

```csharp
protected bool Equals(Size other)
```

##### Parameters

`other` [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

The <code>Size</code> object to compare with the current object.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the specified object  is equal to the current object; otherwise, false.

#### <a id="DotNetBrowser_Geometry_Size_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Geometry_Size_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)
