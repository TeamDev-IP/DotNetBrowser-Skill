# <a id="DotNetBrowser_Geometry_Point"></a> Class Point

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a pair of numbers that in general are used to define coordinates in the
two-dimensional space.

```csharp
public sealed class Point
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Point](DotNetBrowser.Geometry.Point.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Geometry_Point__ctor_System_Int32_System_Int32_"></a> Point\(int, int\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Point" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">x</code> and
<code class="paramref">y</code> coordinates.

```csharp
public Point(int x, int y)
```

#### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The horizontal coordinate.

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The vertical coordinate.

## Fields

### <a id="DotNetBrowser_Geometry_Point_Empty"></a> Empty

An empty <code>Point</code> that has x and y values set to zero.

```csharp
public static readonly Point Empty
```

#### Field Value

 [Point](DotNetBrowser.Geometry.Point.md)

## Properties

### <a id="DotNetBrowser_Geometry_Point_X"></a> X

Gets the horizontal coordinate.

```csharp
public int X { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Geometry_Point_Y"></a> Y

Gets the vertical coordinate.

```csharp
public int Y { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="DotNetBrowser_Geometry_Point_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Point_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Geometry_Point_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

