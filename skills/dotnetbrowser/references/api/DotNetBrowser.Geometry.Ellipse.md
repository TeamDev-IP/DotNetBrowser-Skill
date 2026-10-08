# <a id="DotNetBrowser_Geometry_Ellipse"></a> Class Ellipse

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a three numbers that are used to define ellipse size and orientation in the
two-dimensional space.

```csharp
public sealed class Ellipse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Ellipse](DotNetBrowser.Geometry.Ellipse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Geometry_Ellipse__ctor_System_Single_System_Single_System_Single_"></a> Ellipse\(float, float, float\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Ellipse" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">radiusX</code> and
<code class="paramref">radiusY</code> radii.

```csharp
public Ellipse(float radiusX, float radiusY, float rotationAngle = 0)
```

#### Parameters

`radiusX` [float](https://learn.microsoft.com/dotnet/api/system.single)

Radius X axis size.

`radiusY` [float](https://learn.microsoft.com/dotnet/api/system.single)

Radius X axis size.

`rotationAngle` [float](https://learn.microsoft.com/dotnet/api/system.single)

Ellipse orientation angle.

## Properties

### <a id="DotNetBrowser_Geometry_Ellipse_RadiusX"></a> RadiusX

Gets radius X axis length.

```csharp
public float RadiusX { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Geometry_Ellipse_RadiusY"></a> RadiusY

Gets radius Y axis length.

```csharp
public float RadiusY { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Geometry_Ellipse_RotationAngle"></a> RotationAngle

Gets ellipse orientation angle.

```csharp
public float RotationAngle { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

## Methods

### <a id="DotNetBrowser_Geometry_Ellipse_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Ellipse_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

