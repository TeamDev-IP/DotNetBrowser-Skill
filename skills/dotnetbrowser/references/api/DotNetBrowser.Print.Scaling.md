# <a id="DotNetBrowser_Print_Scaling"></a> Class Scaling

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The scaling used for printing.

```csharp
public sealed class Scaling
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Scaling](DotNetBrowser.Print.Scaling.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Print_Scaling_Default"></a> Default

The default scaling for the printing content.

```csharp
public static readonly Scaling Default
```

#### Field Value

 [Scaling](DotNetBrowser.Print.Scaling.md)

## Methods

### <a id="DotNetBrowser_Print_Scaling_Custom_System_Int32_"></a> Custom\(int\)

Creates a custom scaling which scales the content according to the given scale factor.

```csharp
public static Scaling Custom(int scaleFactor)
```

#### Parameters

`scaleFactor` [int](https://learn.microsoft.com/dotnet/api/system.int32)

       The scale factor to apply to the content, where 

       <pre><code class="lang-csharp">100</code></pre>

is a normal size. Should
       be in the range from 

       <pre><code class="lang-csharp">10</code></pre>

to 

<pre><code class="lang-csharp">200</code></pre>

.

#### Returns

 [Scaling](DotNetBrowser.Print.Scaling.md)

The scaling used for printing.

#### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

       The <code class="paramref">scaleFactor</code> is out of range.
       Should be in the range from 

       <pre><code class="lang-csharp">10</code></pre>

to 

<pre><code class="lang-csharp">200</code></pre>

.

### <a id="DotNetBrowser_Print_Scaling_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_Scaling_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

