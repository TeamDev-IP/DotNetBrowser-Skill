# <a id="DotNetBrowser_Frames_IWebStorage"></a> Interface IWebStorage

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

<p>An HTML WebStorage.</p>
<p>
    Provides access to the session storage or local storage for a particular document on the loaded
    web page. Allows you to add, modify, or delete the stored items.
</p>

```csharp
public interface IWebStorage : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Frames_IWebStorage_Count"></a> Count

Gets the number of the key/value pairs in the storage.

```csharp
int Count { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

### <a id="DotNetBrowser_Frames_IWebStorage_Keys"></a> Keys

Gets a list of the web storage keys.

```csharp
IReadOnlyList<string> Keys { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IWebStorage_Item_System_String_"></a> this\[string\]

Gets or sets the value associated with the given <code class="paramref">key</code>. The setter adds the item with the
specified <code class="paramref">key</code> and
<code class="paramref">value</code> to the storage, or updates it if the item with the given <code class="paramref">key</code> already
exists.

```csharp
string this[string key] { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

## Methods

### <a id="DotNetBrowser_Frames_IWebStorage_Clear"></a> Clear\(\)

Removes all the items from the storage.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

### <a id="DotNetBrowser_Frames_IWebStorage_Contains_System_String_"></a> Contains\(string\)

Checks if the specified key is present in the storage.

```csharp
bool Contains(string key)
```

#### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

the key name to check. Can be empty or blank.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the storage contains an item with the specified <code class="paramref">key</code>,
otherwise <code>false</code>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

### <a id="DotNetBrowser_Frames_IWebStorage_Remove_System_String_"></a> Remove\(string\)

Removes the item with the specified <code class="paramref">key</code> from the storage. Does nothing if there is no
item with the specified <code class="paramref">key</code> in the storage.

```csharp
void Remove(string key)
```

#### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

the key name of the item to remove. Can be empty or blank.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

