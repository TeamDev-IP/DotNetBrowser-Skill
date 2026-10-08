# <a id="DotNetBrowser_SpellCheck_ILanguages"></a> Interface ILanguages

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

The collection of the languages used for spell checking.

```csharp
public interface ILanguages
```

## Properties

### <a id="DotNetBrowser_SpellCheck_ILanguages_All"></a> All

Gets the list of all the languages currently used for spell checking.

```csharp
IReadOnlyList<Language> All { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Language](DotNetBrowser.SpellCheck.Language.md)\>

#### Remarks

<p>
    On Linux and Windows the dictionaries for spell checking are downloaded
    programmatically and stored in the user data directory.
</p>
<p>
    On macOS returns the languages for spell checking configured in the system settings.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_SpellCheck_ILanguages_Add_DotNetBrowser_SpellCheck_Language_"></a> Add\(Language\)

Adds the language to the list of the languages for which spell checking is performed.

```csharp
Task Add(Language language)
```

#### Parameters

`language` [Language](DotNetBrowser.SpellCheck.Language.md)

The language to use for spell checking.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

The task that can be used to wait until the dictionary is loaded from the user data directory.
The task will fail with <xref href="DotNetBrowser.SpellCheck.LanguageNotAvailableException" data-throw-if-not-resolved="false"></xref>
if Chromium fails to download the dictionary for the given language (Windows and Linux),
or the dictionary is not available in the system (macOS).

#### Remarks

<p>
    On Windows and Linux, this method loads the dictionary for the given language and blocks
    the current thread execution until the dictionary is loaded from the user data directory.
    If the dictionary does not exist in the user data directory, the engine will download
    it from the remote server.
</p>
<p>
    On macOS, this method checks whether the specified dictionaries are present in the system,
    and throws a <xref href="DotNetBrowser.SpellCheck.LanguageNotAvailableException" data-throw-if-not-resolved="false"></xref> if not.
</p>

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The language is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_SpellCheck_ILanguages_Remove_DotNetBrowser_SpellCheck_Language_"></a> Remove\(Language\)

Removes the language from the list of the languages for which spell checking is performed.

```csharp
void Remove(Language language)
```

#### Parameters

`language` [Language](DotNetBrowser.SpellCheck.Language.md)

#### Remarks

<p>
    If all languages are removed, Chromium performs no spell checking. To enable spell
    checking, add a language using the <xref href="DotNetBrowser.SpellCheck.ILanguages.Add(DotNetBrowser.SpellCheck.Language)" data-throw-if-not-resolved="false"></xref> method.
</p>
<p>
    On macOS, this method does nothing because spellcheck languages are configured
    in the OS settings.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

