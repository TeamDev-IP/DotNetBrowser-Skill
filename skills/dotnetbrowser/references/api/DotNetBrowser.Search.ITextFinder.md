# <a id="DotNetBrowser_Search_ITextFinder"></a> Interface ITextFinder

Namespace: [DotNetBrowser.Search](DotNetBrowser.Search.md)  
Assembly: DotNetBrowser.dll  

Allows finding text on the loaded web page.

```csharp
public interface ITextFinder : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Search_ITextFinder_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

## Methods

### <a id="DotNetBrowser_Search_ITextFinder_Find_System_String_DotNetBrowser_Search_FindOptions_DotNetBrowser_Handlers_IHandler_DotNetBrowser_Search_Handlers_FindResultReceivedParameters__"></a> Find\(string, FindOptions, IHandler<FindResultReceivedParameters\>\)

Performs search of the given <code class="paramref">searchText</code> with the given <code class="paramref">options</code>,
highlights all matches and selects the first match on the currently loaded web page.

```csharp
Task<FindResult> Find(string searchText, FindOptions options = null, IHandler<FindResultReceivedParameters> intermediateResultsHandler = null)
```

#### Parameters

`searchText` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to search. Cannot be null or empty.

`options` [FindOptions](DotNetBrowser.Search.FindOptions.md)

the options such as direction and match case.

`intermediateResultsHandler` [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[FindResultReceivedParameters](DotNetBrowser.Search.Handlers.FindResultReceivedParameters.md)\>

the handler which is called when some search results are received.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[FindResult](DotNetBrowser.Search.FindResult.md)\>

a <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> which completes when the search is finished. The result of the task is the last find
result received from Chromium.

#### Remarks

The search is performed only through a visible content on the loaded web page. If some text
is presented on the web page, but due to CSS rules it's not visible, the text finder will not
check this content during search. Also, it doesn't find text on the web pages with an empty
size, so make sure that the size of the browser instance where the text search is performed
isn't empty.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Search_ITextFinder_StopFinding_DotNetBrowser_Search_StopFindAction_"></a> StopFinding\(StopFindAction\)

Stops finding and clears the highlighting of the found matches.

```csharp
void StopFinding(StopFindAction action = StopFindAction.ClearSelection)
```

#### Parameters

`action` [StopFindAction](DotNetBrowser.Search.StopFindAction.md)

The action that will be applied to the selected match.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> has already been disposed.

