# <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary"></a> Interface ISpellCheckDictionary

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

Provides functionality for working with a spell check dictionary.

```csharp
public interface ISpellCheckDictionary : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Words"></a> Words

Gets the words in the dictionary.

```csharp
IEnumerable<string> Words { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Add_System_String_"></a> Add\(string\)

Adds the specified <code class="paramref">word</code> to the dictionary and schedules a write to disk.

```csharp
bool Add(string word)
```

#### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to add to the dictionary. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the word is valid and not a duplicate.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Contains_System_String_"></a> Contains\(string\)

Checks if the dictionary contains the specified <code class="paramref">word</code>.

```csharp
bool Contains(string word)
```

#### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to check. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the word is present in the dictionary, <code>false</code> otherwise.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Remove_System_String_"></a> Remove\(string\)

Removes the specified <code class="paramref">word</code> from the dictionary.

```csharp
bool Remove(string word)
```

#### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to remove from the dictionary. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code>  if the word was found and removed successfully, <code>false</code> otherwise.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

