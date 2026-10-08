# <a id="DotNetBrowser_Search_FindOptions"></a> Class FindOptions

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

The find text options.

```csharp
public class FindOptions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FindOptions](DotNetBrowser.Search.FindOptions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Search_FindOptions__ctor_System_Boolean_DotNetBrowser_Search_Direction_"></a> FindOptions\(bool, Direction\)

Initializes a new instance of <xref href="DotNetBrowser.Search.FindOptions" data-throw-if-not-resolved="false"></xref> with the specified <code class="paramref">matchCase</code> and
<code class="paramref">direction</code>.

```csharp
public FindOptions(bool matchCase = false, Direction direction = Direction.Forward)
```

#### Parameters

`matchCase` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether the search is case-sensitive.

`direction` [Direction](DotNetBrowser.Search.Direction.md)

The search direction.

## Properties

### <a id="DotNetBrowser_Search_FindOptions_Direction"></a> Direction

Gets or sets the search direction.

```csharp
public Direction Direction { get; set; }
```

#### Property Value

 [Direction](DotNetBrowser.Search.Direction.md)

### <a id="DotNetBrowser_Search_FindOptions_MatchCase"></a> MatchCase

Enables or disables the case-sensitive search.

```csharp
public bool MatchCase { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

