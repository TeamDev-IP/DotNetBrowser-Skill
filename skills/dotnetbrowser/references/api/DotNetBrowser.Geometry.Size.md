# <a id="DotNetBrowser_Geometry_Size"></a> Class Size

Namespace: [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)  
Assembly: DotNetBrowser.dll  

Represents a pair of numbers that in general are used to define dimensions in the
two-dimensional space.

```csharp
public class Size
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Size](DotNetBrowser.Geometry.Size.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Geometry_Size__ctor_System_UInt32_System_UInt32_"></a> Size\(uint, uint\)

Initializes a new instance of the <xref href="DotNetBrowser.Geometry.Size" data-throw-if-not-resolved="false"></xref> class with the specified <code class="paramref">width</code> and
<code class="paramref">height</code>.

```csharp
public Size(uint width, uint height)
```

#### Parameters

`width` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

the horizontal dimension. Cannot be negative.

`height` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

the vertical dimension. Cannot be negative.

## Fields

### <a id="DotNetBrowser_Geometry_Size_Empty"></a> Empty

An empty <code>Size</code> that has x and y values set to zero.

```csharp
public static readonly Size Empty
```

#### Field Value

 [Size](DotNetBrowser.Geometry.Size.md)

## Properties

### <a id="DotNetBrowser_Geometry_Size_Height"></a> Height

Gets the vertical dimension.

```csharp
public uint Height { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Geometry_Size_IsEmpty"></a> IsEmpty

Indicates whether width and height of this Size have values of zero.

```csharp
public bool IsEmpty { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Size_Width"></a> Width

Gets the horizontal dimension.

```csharp
public uint Width { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

## Methods

### <a id="DotNetBrowser_Geometry_Size_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Geometry_Size_Equals_DotNetBrowser_Geometry_Size_"></a> Equals\(Size\)

Determines whether the specified <code>Size</code> object is equal to the current object.

```csharp
protected bool Equals(Size other)
```

#### Parameters

`other` [Size](DotNetBrowser.Geometry.Size.md)

The <code>Size</code> object to compare with the current object.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the specified object  is equal to the current object; otherwise, false.

### <a id="DotNetBrowser_Geometry_Size_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Geometry_Size_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

