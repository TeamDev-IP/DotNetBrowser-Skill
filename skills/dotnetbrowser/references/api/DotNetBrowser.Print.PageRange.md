# <a id="DotNetBrowser_Print_PageRange"></a> Class PageRange

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The page range to be printed.

```csharp
public sealed class PageRange
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageRange](DotNetBrowser.Print.PageRange.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Print_PageRange__ctor_System_Int32_System_Int32_"></a> PageRange\(int, int\)

Creates a new page range instance.

```csharp
public PageRange(int from, int to)
```

#### Parameters

`from` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The 1-based number of the first page within the range.

`to` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The 1-based number of the last page within the range.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">from</code> is greater than <code class="paramref">to</code>.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">from</code> is less than or equal to zero.

## Properties

### <a id="DotNetBrowser_Print_PageRange_From"></a> From

Gets the number of the first page within the range.

```csharp
public int From { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Print_PageRange_To"></a> To

Gets the number of the last page within the range.

```csharp
public int To { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="DotNetBrowser_Print_PageRange_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_PageRange_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

