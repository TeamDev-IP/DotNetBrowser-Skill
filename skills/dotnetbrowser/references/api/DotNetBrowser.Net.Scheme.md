# <a id="DotNetBrowser_Net_Scheme"></a> Class Scheme

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The scheme component of a URL.

```csharp
public sealed class Scheme : TypedEnum<string>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[Scheme](DotNetBrowser.Net.Scheme.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Net_Scheme_Http"></a> Http

The HTTP scheme.

```csharp
public static readonly Scheme Http
```

#### Field Value

 [Scheme](DotNetBrowser.Net.Scheme.md)

### <a id="DotNetBrowser_Net_Scheme_Https"></a> Https

The HTTPS scheme.

```csharp
public static readonly Scheme Https
```

#### Field Value

 [Scheme](DotNetBrowser.Net.Scheme.md)

## Properties

### <a id="DotNetBrowser_Net_Scheme_IsInterceptable"></a> IsInterceptable

Indicates whether this scheme is interceptable.

```csharp
public bool IsInterceptable { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## Methods

### <a id="DotNetBrowser_Net_Scheme_Create_System_String_"></a> Create\(string\)

Creates the Scheme instance from string representation.

```csharp
public static Scheme Create(string value)
```

#### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

#### Returns

 [Scheme](DotNetBrowser.Net.Scheme.md)

the corresponding <xref href="DotNetBrowser.Net.Scheme" data-throw-if-not-resolved="false"></xref> instance.

## Operators

### <a id="DotNetBrowser_Net_Scheme_op_Explicit_System_String__DotNetBrowser_Net_Scheme"></a> explicit operator Scheme\(string\)

Creates the Scheme instance from string representation.

```csharp
public static explicit operator Scheme(string value)
```

#### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

string representation

#### Returns

 [Scheme](DotNetBrowser.Net.Scheme.md)

the corresponding <xref href="DotNetBrowser.Net.Scheme" data-throw-if-not-resolved="false"></xref> instance.

