# <a id="DotNetBrowser_SpellCheck_ISpellChecker"></a> Interface ISpellChecker

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

Represents an engine service that provides functionality for configuring spell checking.

```csharp
public interface ISpellChecker : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_SpellCheck_ISpellChecker_CustomDictionary"></a> CustomDictionary

Gets the custom dictionary.

```csharp
ISpellCheckDictionary CustomDictionary { get; }
```

#### Property Value

 [ISpellCheckDictionary](DotNetBrowser.SpellCheck.ISpellCheckDictionary.md)

### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Enabled"></a> Enabled

Enables or disables spell checking. By default, spell checking is enabled.

```csharp
bool Enabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Engine"></a> Engine

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Languages"></a> Languages

Gets the list of the languages used for spell checking.

```csharp
ILanguages Languages { get; }
```

#### Property Value

 [ILanguages](DotNetBrowser.SpellCheck.ILanguages.md)

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

