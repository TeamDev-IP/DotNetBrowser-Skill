# <a id="DotNetBrowser_SpellCheck_SpellCheckingResult"></a> Class SpellCheckingResult

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

The spell checking result that contains the bounds of a mis-spelled substring of the
checked text.

```csharp
public sealed class SpellCheckingResult
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SpellCheckingResult](DotNetBrowser.SpellCheck.SpellCheckingResult.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_SpellCheck_SpellCheckingResult_Length"></a> Length

Gets the length of the mis-spelled word in the checked text.

```csharp
public uint Length { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_SpellCheck_SpellCheckingResult_Location"></a> Location

Gets the location of the first symbol in the mis-spelled word in the checked text that is
considered as mis-spelled by the spell checker.

```csharp
public uint Location { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

