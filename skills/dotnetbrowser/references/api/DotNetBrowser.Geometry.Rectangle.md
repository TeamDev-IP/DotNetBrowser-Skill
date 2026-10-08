# <a id="DotNetBrowser_Geometry_Rectangle"></a> Class Rectangle

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a rectangle described by the location and dimensions.

```csharp
public sealed class Rectangle
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Rectangle](DotNetBrowser.Geometry.Rectangle.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Geometry_Rectangle__ctor_DotNetBrowser_Geometry_Point_DotNetBrowser_Geometry_Size_"></a> Rectangle\(Point, Size\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">origin</code> and
<code class="paramref">size</code>.

```csharp
public Rectangle(Point origin, Size size)
```

#### Parameters

`origin` [Point](DotNetBrowser.Geometry.Point.md)

The top-left corner coordinate of the rectangle.

`size` [Size](DotNetBrowser.Geometry.Size.md)

The rectangle dimensions.

### <a id="DotNetBrowser_Geometry_Rectangle__ctor_System_Int32_System_Int32_System_UInt32_System_UInt32_"></a> Rectangle\(int, int, uint, uint\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> class with the specified parameters.

```csharp
public Rectangle(int x, int y, uint width, uint height)
```

#### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The top-left corner X coordinate of the rectangle.

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The top-left corner Y coordinate of the rectangle.

`width` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The rectangle width.

`height` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The rectangle height.

## Properties

### <a id="DotNetBrowser_Geometry_Rectangle_IsEmpty"></a> IsEmpty

Indicates whether all numeric properties of this Rectangle have values of zero.

```csharp
public bool IsEmpty { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Rectangle_Origin"></a> Origin

Gets the top-left corner coordinate of the rectangle.

```csharp
public Point Origin { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Geometry_Rectangle_Size"></a> Size

Gets the rectangle dimensions.

```csharp
public Size Size { get; }
```

#### Property Value

 [Size](DotNetBrowser.Geometry.Size.md)

## Methods

### <a id="DotNetBrowser_Geometry_Rectangle_Center"></a> Center\(\)

Calculates the center of this rectangle.

```csharp
public Point Center()
```

#### Returns

 [Point](DotNetBrowser.Geometry.Point.md)

The point that represents the center of this rectangle.

### <a id="DotNetBrowser_Geometry_Rectangle_Contains_DotNetBrowser_Geometry_Point_"></a> Contains\(Point\)

Checks whether the rectangle contains the specified point.

```csharp
public bool Contains(Point point)
```

#### Parameters

`point` [Point](DotNetBrowser.Geometry.Point.md)

the <xref href="DotNetBrowser.Geometry.Point" data-throw-if-not-resolved="false"></xref> instance to check.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the rectangle contains this point; false otherwise.

### <a id="DotNetBrowser_Geometry_Rectangle_Contains_DotNetBrowser_Geometry_Rectangle_"></a> Contains\(Rectangle\)

Checks whether the rectangle contains the specified rectangle.

```csharp
public bool Contains(Rectangle other)
```

#### Parameters

`other` [Rectangle](DotNetBrowser.Geometry.Rectangle.md)

the <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> instance to check.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the rectangle contains the other rectangle; false otherwise.

### <a id="DotNetBrowser_Geometry_Rectangle_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Rectangle_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Geometry_Rectangle_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

