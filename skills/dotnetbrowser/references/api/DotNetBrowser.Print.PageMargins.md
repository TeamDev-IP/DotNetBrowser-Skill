# <a id="DotNetBrowser_Print_PageMargins"></a> Class PageMargins

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The page margins used for printing.

```csharp
public sealed class PageMargins
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageMargins](DotNetBrowser.Print.PageMargins.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Print_PageMargins__ctor_System_Int32_System_Int32_System_Int32_System_Int32_"></a> PageMargins\(int, int, int, int\)

Creates custom margins for the web page in points. One point equals 1/72 of an inch.

```csharp
public PageMargins(int left, int right, int top, int bottom)
```

#### Parameters

`left` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the left side of the sheet. Cannot be negative.

`right` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the right side of the sheet. Cannot be negative.

`top` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the top side of the sheet. Cannot be negative.

`bottom` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the bottom side of the sheet. Cannot be negative.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Any of the parameters is negative.

## Fields

### <a id="DotNetBrowser_Print_PageMargins_Default"></a> Default

The default margins for the page.

```csharp
public static readonly PageMargins Default
```

#### Field Value

 [PageMargins](DotNetBrowser.Print.PageMargins.md)

### <a id="DotNetBrowser_Print_PageMargins_None"></a> None

The empty margins for the page.

```csharp
public static readonly PageMargins None
```

#### Field Value

 [PageMargins](DotNetBrowser.Print.PageMargins.md)

## Properties

### <a id="DotNetBrowser_Print_PageMargins_Bottom"></a> Bottom

Gets the margin on the bottom side of the sheet.

```csharp
public int Bottom { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Print_PageMargins_Left"></a> Left

Gets the margin on the left side of the sheet.

```csharp
public int Left { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Print_PageMargins_Right"></a> Right

Gets the margin on the right side of the sheet.

```csharp
public int Right { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Print_PageMargins_Top"></a> Top

Gets the margin on the top side of the sheet.

```csharp
public int Top { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="DotNetBrowser_Print_PageMargins_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_PageMargins_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

