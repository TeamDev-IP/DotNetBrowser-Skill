# <a id="DotNetBrowser_Navigation_INavigationEntry"></a> Interface INavigationEntry

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The navigation history entry.

```csharp
public interface INavigationEntry
```

## Properties

### <a id="DotNetBrowser_Navigation_INavigationEntry_HttpStatusCode"></a> HttpStatusCode

Gets the status code of the last known successful navigation.

```csharp
int HttpStatusCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Navigation_INavigationEntry_OriginalRequestUrl"></a> OriginalRequestUrl

Gets the URL that caused this entry to be created.

```csharp
string OriginalRequestUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Navigation_INavigationEntry_PageType"></a> PageType

Gets the page type that tells if this entry is for an interstitial or error page.

```csharp
PageType PageType { get; }
```

#### Property Value

 [PageType](DotNetBrowser.Navigation.PageType.md)

### <a id="DotNetBrowser_Navigation_INavigationEntry_Timestamp"></a> Timestamp

Gets the time at which the last known local navigation was completed.

```csharp
DateTime? Timestamp { get; }
```

#### Property Value

 [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)?

### <a id="DotNetBrowser_Navigation_INavigationEntry_Title"></a> Title

Gets the title as set by the page. This value is empty if there is no title set.

```csharp
string Title { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Navigation_INavigationEntry_Url"></a> Url

Gets the actual URL of the web page.

```csharp
string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

