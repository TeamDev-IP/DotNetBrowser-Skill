# <a id="DotNetBrowser_Ui_FontSize"></a> Class FontSize

Namespace: [DotNetBrowser.Ui](DotNetBrowser.Ui.md)  
Assembly: DotNetBrowser.dll  

The browser font size.

```csharp
public sealed class FontSize
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FontSize](DotNetBrowser.Ui.FontSize.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Ui_FontSize__ctor_System_Int32_"></a> FontSize\(int\)

Creates a new font size.

```csharp
public FontSize(int value)
```

#### Parameters

`value` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The font size in pixels. Cannot be zero or negative.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The font size in pixels is zero or negative.

## Properties

### <a id="DotNetBrowser_Ui_FontSize_Value"></a> Value

Gets the font size in pixels.

```csharp
public int Value { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="DotNetBrowser_Ui_FontSize_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Ui_FontSize_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Operators

### <a id="DotNetBrowser_Ui_FontSize_op_Implicit_DotNetBrowser_Ui_FontSize__System_Int32"></a> implicit operator int\(FontSize\)

Converts the font size to integer.

```csharp
public static implicit operator int(FontSize size)
```

#### Parameters

`size` [FontSize](DotNetBrowser.Ui.FontSize.md)

The font size to convert.

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Ui_FontSize_op_Implicit_System_Int32__DotNetBrowser_Ui_FontSize"></a> implicit operator FontSize\(int\)

Converts an integer to the font size.

```csharp
public static implicit operator FontSize(int value)
```

#### Parameters

`value` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The font size in pixels. Cannot be zero or negative.

#### Returns

 [FontSize](DotNetBrowser.Ui.FontSize.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The font size in pixels is zero or negative.

