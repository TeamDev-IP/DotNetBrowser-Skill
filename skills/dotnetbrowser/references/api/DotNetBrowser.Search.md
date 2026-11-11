# <a id="DotNetBrowser_Search"></a> Namespace DotNetBrowser.Search

### Namespaces

 [DotNetBrowser.Search.Handlers](DotNetBrowser.Search.Handlers.md)

### Classes

 [FindOptions](DotNetBrowser.Search.md#DotNetBrowser_Search_FindOptions)

The find text options.

 [FindResult](DotNetBrowser.Search.md#DotNetBrowser_Search_FindResult)

A result of the text search.

### Interfaces

 [ITextFinder](DotNetBrowser.Search.md#DotNetBrowser_Search_ITextFinder)

Allows finding text on the loaded web page.

### Enums

 [Direction](DotNetBrowser.Search.md#DotNetBrowser_Search_Direction)

The search direction.

 [StopFindAction](DotNetBrowser.Search.md#DotNetBrowser_Search_StopFindAction)

The stop find actions.

## <a id="DotNetBrowser_Search_FindOptions"></a> Class FindOptions

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

The find text options.

```csharp
public class FindOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FindOptions](DotNetBrowser.Search.md#DotNetBrowser_Search_FindOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Search_FindOptions__ctor_System_Boolean_DotNetBrowser_Search_Direction_"></a> FindOptions\(bool, Direction\)

Initializes a new instance of <xref href="DotNetBrowser.Search.FindOptions" data-throw-if-not-resolved="false"></xref> with the specified <code class="paramref">matchCase</code> and
<code class="paramref">direction</code>.

```csharp
public FindOptions(bool matchCase = false, Direction direction = Direction.Forward)
```

##### Parameters

`matchCase` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether the search is case-sensitive.

`direction` [Direction](DotNetBrowser.Search.md#DotNetBrowser_Search_Direction)

The search direction.

### Properties

#### <a id="DotNetBrowser_Search_FindOptions_Direction"></a> Direction

Gets or sets the search direction.

```csharp
public Direction Direction { get; set; }
```

##### Property Value

 [Direction](DotNetBrowser.Search.md#DotNetBrowser_Search_Direction)

#### <a id="DotNetBrowser_Search_FindOptions_MatchCase"></a> MatchCase

Enables or disables the case-sensitive search.

```csharp
public bool MatchCase { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Search_FindResult"></a> Class FindResult

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

A result of the text search.

```csharp
public class FindResult
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FindResult](DotNetBrowser.Search.md#DotNetBrowser_Search_FindResult)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Search_FindResult_NumberOfMatches"></a> NumberOfMatches

Gets the number of matches.

```csharp
public int NumberOfMatches { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Search_FindResult_SelectedMatch"></a> SelectedMatch

Gets the index of the currently selected match.

```csharp
public int SelectedMatch { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Search_ITextFinder"></a> Interface ITextFinder

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

Allows finding text on the loaded web page.

```csharp
public interface ITextFinder : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Search_ITextFinder_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

### Methods

#### <a id="DotNetBrowser_Search_ITextFinder_Find_System_String_DotNetBrowser_Search_FindOptions_DotNetBrowser_Handlers_IHandler_DotNetBrowser_Search_Handlers_FindResultReceivedParameters__"></a> Find\(string, FindOptions, IHandler<FindResultReceivedParameters\>\)

Performs search of the given <code class="paramref">searchText</code> with the given <code class="paramref">options</code>,
highlights all matches and selects the first match on the currently loaded web page.

```csharp
Task<FindResult> Find(string searchText, FindOptions options = null, IHandler<FindResultReceivedParameters> intermediateResultsHandler = null)
```

##### Parameters

`searchText` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to search. Cannot be null or empty.

`options` [FindOptions](DotNetBrowser.Search.md#DotNetBrowser_Search_FindOptions)

the options such as direction and match case.

`intermediateResultsHandler` [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[FindResultReceivedParameters](DotNetBrowser.Search.Handlers.md#DotNetBrowser_Search_Handlers_FindResultReceivedParameters)\>

the handler which is called when some search results are received.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[FindResult](DotNetBrowser.Search.md#DotNetBrowser_Search_FindResult)\>

a <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> which completes when the search is finished. The result of the task is the last find
result received from Chromium.

##### Remarks

The search is performed only through a visible content on the loaded web page. If some text
is presented on the web page, but due to CSS rules it's not visible, the text finder will not
check this content during search. Also, it doesn't find text on the web pages with an empty
size, so make sure that the size of the browser instance where the text search is performed
isn't empty.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Search_ITextFinder_StopFinding_DotNetBrowser_Search_StopFindAction_"></a> StopFinding\(StopFindAction\)

Stops finding and clears the highlighting of the found matches.

```csharp
void StopFinding(StopFindAction action = StopFindAction.ClearSelection)
```

##### Parameters

`action` [StopFindAction](DotNetBrowser.Search.md#DotNetBrowser_Search_StopFindAction)

The action that will be applied to the selected match.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Search_Direction"></a> Enum Direction

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

The search direction.

```csharp
public enum Direction
```

### Fields

`Backward = 2` 

Search backward.



`Forward = 1` 

Search forward.

## <a id="DotNetBrowser_Search_StopFindAction"></a> Enum StopFindAction

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

The stop find actions.

```csharp
public enum StopFindAction
```

### Fields

`ClearSelection = 1` 

Stops the current search and clears the selection.



`KeepSelection = 2` 

Stops the current search but leave the selection.
