# <a id="DotNetBrowser_Search_Handlers_FindResultReceivedParameters"></a> Class FindResultReceivedParameters

Namespace: [DotNetBrowser.Search.Handlers](DotNetBrowser.Search.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the handler that is passed to the <xref href="DotNetBrowser.Search.ITextFinder.Find(System.String%2cDotNetBrowser.Search.FindOptions%2cDotNetBrowser.Handlers.IHandler%7bDotNetBrowser.Search.Handlers.FindResultReceivedParameters%7d)" data-throw-if-not-resolved="false"></xref>
method and called when a find result is received.

```csharp
public sealed class FindResultReceivedParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FindResultReceivedParameters](DotNetBrowser.Search.Handlers.FindResultReceivedParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Search_Handlers_FindResultReceivedParameters_FindResult"></a> FindResult

Gets the find result.

```csharp
public FindResult FindResult { get; }
```

#### Property Value

 [FindResult](DotNetBrowser.Search.FindResult.md)

### <a id="DotNetBrowser_Search_Handlers_FindResultReceivedParameters_IsSearchFinished"></a> IsSearchFinished

Indicates whether the searching process was finished.

```csharp
public bool IsSearchFinished { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Search_Handlers_FindResultReceivedParameters_TextFinder"></a> TextFinder

Gets the <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
public ITextFinder TextFinder { get; }
```

#### Property Value

 [ITextFinder](DotNetBrowser.Search.ITextFinder.md)

## Methods

### <a id="DotNetBrowser_Search_Handlers_FindResultReceivedParameters_ToString"></a> ToString\(\)

Represent object as string

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the object

