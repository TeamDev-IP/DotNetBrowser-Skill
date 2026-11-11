# <a id="DotNetBrowser_SpellCheck"></a> Namespace DotNetBrowser.SpellCheck

### Classes

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The language for which Chromium can perform spell checking.

 [LanguageNotAvailableException](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_LanguageNotAvailableException)

Thrown when the engine fails to configure the spellchecker to use the language
passed to the <xref href="DotNetBrowser.SpellCheck.ILanguages.Add(DotNetBrowser.SpellCheck.Language)" data-throw-if-not-resolved="false"></xref> method.

 [SpellCheckMenu](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_SpellCheckMenu)

A spell check menu in the context menu.

 [SpellCheckingResult](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_SpellCheckingResult)

The spell checking result that contains the bounds of a mis-spelled substring of the
checked text.

### Interfaces

 [ILanguages](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ILanguages)

The collection of the languages used for spell checking.

 [ISpellCheckDictionary](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ISpellCheckDictionary)

Provides functionality for working with a spell check dictionary.

 [ISpellChecker](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ISpellChecker)

Represents an engine service that provides functionality for configuring spell checking.

## <a id="DotNetBrowser_SpellCheck_Language"></a> Class Language

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

The language for which Chromium can perform spell checking.

```csharp
public sealed class Language : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_SpellCheck_Language_Bulgarian"></a> Bulgarian

Bulgarian language ("bg")

```csharp
public static readonly Language Bulgarian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Catalan"></a> Catalan

Catalan language ("ca")

```csharp
public static readonly Language Catalan
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Croatian"></a> Croatian

Croatian language ("hr")

```csharp
public static readonly Language Croatian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Czech"></a> Czech

Czech language ("cs")

```csharp
public static readonly Language Czech
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Danish"></a> Danish

Danish language ("da")

```csharp
public static readonly Language Danish
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Default"></a> Default

Default language (English).

```csharp
public static readonly Language Default
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Dutch"></a> Dutch

Dutch language ("nl")

```csharp
public static readonly Language Dutch
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_EnglishUk"></a> EnglishUk

English (UK) language ("en-gb")

```csharp
public static readonly Language EnglishUk
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_EnglishUs"></a> EnglishUs

English (US) language ("en-us")

```csharp
public static readonly Language EnglishUs
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Estonian"></a> Estonian

Estonian language ("et")

```csharp
public static readonly Language Estonian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_French"></a> French

French (France) language ("fr")

```csharp
public static readonly Language French
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_German"></a> German

German language ("de")

```csharp
public static readonly Language German
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Greek"></a> Greek

Greek language ("el")

```csharp
public static readonly Language Greek
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Hebrew"></a> Hebrew

Hebrew language ("he")

```csharp
public static readonly Language Hebrew
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Hindi"></a> Hindi

Hindi language ("hi")

```csharp
public static readonly Language Hindi
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Hungarian"></a> Hungarian

Hungarian language ("hu")

```csharp
public static readonly Language Hungarian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Indonesian"></a> Indonesian

Indonesian language ("id")

```csharp
public static readonly Language Indonesian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Italian"></a> Italian

Italian language ("it")

```csharp
public static readonly Language Italian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Korean"></a> Korean

Korean language ("ko")

```csharp
public static readonly Language Korean
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Latvian"></a> Latvian

Latvian language ("lv")

```csharp
public static readonly Language Latvian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Lithuanian"></a> Lithuanian

Lithuanian language ("lt")

```csharp
public static readonly Language Lithuanian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Norwegian"></a> Norwegian

Norwegian language ("nb")

```csharp
public static readonly Language Norwegian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Persian"></a> Persian

Persian language ("fa")

```csharp
public static readonly Language Persian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Polish"></a> Polish

Polish language ("pl")

```csharp
public static readonly Language Polish
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_PortugueseBrazil"></a> PortugueseBrazil

Portuguese (Brazil) language ("pt-br")

```csharp
public static readonly Language PortugueseBrazil
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_PortuguesePortugal"></a> PortuguesePortugal

Portuguese (Portugal) language ("pt-pt")

```csharp
public static readonly Language PortuguesePortugal
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Romanian"></a> Romanian

Romanian language ("ro")

```csharp
public static readonly Language Romanian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Russian"></a> Russian

Russian language ("ru")

```csharp
public static readonly Language Russian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Serbian"></a> Serbian

Serbian language ("sr")

```csharp
public static readonly Language Serbian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Slovak"></a> Slovak

Slovak language ("sk")

```csharp
public static readonly Language Slovak
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Slovenian"></a> Slovenian

Slovenian language ("sl")

```csharp
public static readonly Language Slovenian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_SpanishSpain"></a> SpanishSpain

Spanish language (Spain) ("es")

```csharp
public static readonly Language SpanishSpain
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Swedish"></a> Swedish

Swedish language ("sv")

```csharp
public static readonly Language Swedish
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Turkish"></a> Turkish

Turkish language ("tr")

```csharp
public static readonly Language Turkish
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Ukrainian"></a> Ukrainian

Ukrainian language ("uk")

```csharp
public static readonly Language Ukrainian
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

#### <a id="DotNetBrowser_SpellCheck_Language_Vietnamese"></a> Vietnamese

Vietnamese language ("vi")

```csharp
public static readonly Language Vietnamese
```

##### Field Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

### Properties

#### <a id="DotNetBrowser_SpellCheck_Language_Code"></a> Code

Gets the language code.

```csharp
public string Code { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_SpellCheck_Language_Region"></a> Region

Gets the region code. Empty if the region is not specified.

```csharp
public string Region { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_SpellCheck_Language_Create_System_String_System_String_"></a> Create\(string, string\)

Initializes the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance with the given <xref href="DotNetBrowser.SpellCheck.Language.Code" data-throw-if-not-resolved="false"></xref>
and <xref href="DotNetBrowser.SpellCheck.Language.Region" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Language Create(string code, string region)
```

##### Parameters

`code` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language code.

`region` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language code.

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_SpellCheck_Language_Create_System_String_"></a> Create\(string\)

Initializes the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance with the given <xref href="DotNetBrowser.SpellCheck.Language.Code" data-throw-if-not-resolved="false"></xref>.

```csharp
public static Language Create(string code)
```

##### Parameters

`code` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language code.

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_SpellCheck_Language_FromCulture_System_Globalization_CultureInfo_"></a> FromCulture\(CultureInfo\)

Initializes the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance from the specified culture information.

```csharp
public static Language FromCulture(CultureInfo cultureInfo)
```

##### Parameters

`cultureInfo` [CultureInfo](https://learn.microsoft.com/dotnet/api/system.globalization.cultureinfo)

The culture information.

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_SpellCheck_Language_FromString_System_String_"></a> FromString\(string\)

Returns the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static Language FromString(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language string representation

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.

### Operators

#### <a id="DotNetBrowser_SpellCheck_Language_op_Explicit_System_Globalization_CultureInfo__DotNetBrowser_SpellCheck_Language"></a> explicit operator Language\(CultureInfo\)

Returns the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance by the specified culture information.

```csharp
public static explicit operator Language(CultureInfo cultureInfo)
```

##### Parameters

`cultureInfo` [CultureInfo](https://learn.microsoft.com/dotnet/api/system.globalization.cultureinfo)

The culture information.

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the specified culture information.

#### <a id="DotNetBrowser_SpellCheck_Language_op_Explicit_System_String__DotNetBrowser_SpellCheck_Language"></a> explicit operator Language\(string\)

Returns the <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static explicit operator Language(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The language string representation

##### Returns

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The <xref href="DotNetBrowser.SpellCheck.Language" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.

## <a id="DotNetBrowser_SpellCheck_LanguageNotAvailableException"></a> Class LanguageNotAvailableException

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

Thrown when the engine fails to configure the spellchecker to use the language
passed to the <xref href="DotNetBrowser.SpellCheck.ILanguages.Add(DotNetBrowser.SpellCheck.Language)" data-throw-if-not-resolved="false"></xref> method.

```csharp
public sealed class LanguageNotAvailableException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[LanguageNotAvailableException](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_LanguageNotAvailableException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_SpellCheck_LanguageNotAvailableException_Language"></a> Language

Gets the language for which the dictionary is not available.

```csharp
public Language Language { get; }
```

##### Property Value

 [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

## <a id="DotNetBrowser_SpellCheck_SpellCheckMenu"></a> Class SpellCheckMenu

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

A spell check menu in the context menu.

```csharp
public sealed class SpellCheckMenu
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SpellCheckMenu](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_SpellCheckMenu)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_AddToDictionaryMenuItemText"></a> AddToDictionaryMenuItemText

Gets the localized text of the "Add to Dictionary" menu item.

```csharp
public string AddToDictionaryMenuItemText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_DictionarySuggestions"></a> DictionarySuggestions

Gets a collection of the suggested replacements for a misspelled word under the cursor.

```csharp
public IEnumerable<string> DictionarySuggestions { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_MisspelledWord"></a> MisspelledWord

Gets the misspelled word under the cursor, if any.

```csharp
public string MisspelledWord { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_SpellCheck_SpellCheckingResult"></a> Class SpellCheckingResult

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

The spell checking result that contains the bounds of a mis-spelled substring of the
checked text.

```csharp
public sealed class SpellCheckingResult
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SpellCheckingResult](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_SpellCheckingResult)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_SpellCheck_SpellCheckingResult_Length"></a> Length

Gets the length of the mis-spelled word in the checked text.

```csharp
public uint Length { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### <a id="DotNetBrowser_SpellCheck_SpellCheckingResult_Location"></a> Location

Gets the location of the first symbol in the mis-spelled word in the checked text that is
considered as mis-spelled by the spell checker.

```csharp
public uint Location { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

## <a id="DotNetBrowser_SpellCheck_ILanguages"></a> Interface ILanguages

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

The collection of the languages used for spell checking.

```csharp
public interface ILanguages
```

### Properties

#### <a id="DotNetBrowser_SpellCheck_ILanguages_All"></a> All

Gets the list of all the languages currently used for spell checking.

```csharp
IReadOnlyList<Language> All { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)\>

##### Remarks

<p>
    On Linux and Windows the dictionaries for spell checking are downloaded
    programmatically and stored in the user data directory.
</p>
<p>
    On macOS returns the languages for spell checking configured in the system settings.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_SpellCheck_ILanguages_Add_DotNetBrowser_SpellCheck_Language_"></a> Add\(Language\)

Adds the language to the list of the languages for which spell checking is performed.

```csharp
Task Add(Language language)
```

##### Parameters

`language` [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

The language to use for spell checking.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

The task that can be used to wait until the dictionary is loaded from the user data directory.
The task will fail with <xref href="DotNetBrowser.SpellCheck.LanguageNotAvailableException" data-throw-if-not-resolved="false"></xref>
if Chromium fails to download the dictionary for the given language (Windows and Linux),
or the dictionary is not available in the system (macOS).

##### Remarks

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

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The language is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_SpellCheck_ILanguages_Remove_DotNetBrowser_SpellCheck_Language_"></a> Remove\(Language\)

Removes the language from the list of the languages for which spell checking is performed.

```csharp
void Remove(Language language)
```

##### Parameters

`language` [Language](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_Language)

##### Remarks

<p>
    If all languages are removed, Chromium performs no spell checking. To enable spell
    checking, add a language using the <xref href="DotNetBrowser.SpellCheck.ILanguages.Add(DotNetBrowser.SpellCheck.Language)" data-throw-if-not-resolved="false"></xref> method.
</p>
<p>
    On macOS, this method does nothing because spellcheck languages are configured
    in the OS settings.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary"></a> Interface ISpellCheckDictionary

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

Provides functionality for working with a spell check dictionary.

```csharp
public interface ISpellCheckDictionary : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Words"></a> Words

Gets the words in the dictionary.

```csharp
IEnumerable<string> Words { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Add_System_String_"></a> Add\(string\)

Adds the specified <code class="paramref">word</code> to the dictionary and schedules a write to disk.

```csharp
bool Add(string word)
```

##### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to add to the dictionary. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the word is valid and not a duplicate.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Contains_System_String_"></a> Contains\(string\)

Checks if the dictionary contains the specified <code class="paramref">word</code>.

```csharp
bool Contains(string word)
```

##### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to check. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the word is present in the dictionary, <code>false</code> otherwise.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_SpellCheck_ISpellCheckDictionary_Remove_System_String_"></a> Remove\(string\)

Removes the specified <code class="paramref">word</code> from the dictionary.

```csharp
bool Remove(string word)
```

##### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

The word to remove from the dictionary. It must be UTF8, between 1 and 99 bytes long,
and without leading or trailing ASCII whitespace.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code>  if the word was found and removed successfully, <code>false</code> otherwise.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code>is null, empty, or contains only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellCheckDictionary" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_SpellCheck_ISpellChecker"></a> Interface ISpellChecker

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

Represents an engine service that provides functionality for configuring spell checking.

```csharp
public interface ISpellChecker : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_SpellCheck_ISpellChecker_CustomDictionary"></a> CustomDictionary

Gets the custom dictionary.

```csharp
ISpellCheckDictionary CustomDictionary { get; }
```

##### Property Value

 [ISpellCheckDictionary](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ISpellCheckDictionary)

#### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Enabled"></a> Enabled

Enables or disables spell checking. By default, spell checking is enabled.

```csharp
bool Enabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Engine"></a> Engine

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_SpellCheck_ISpellChecker_Languages"></a> Languages

Gets the list of the languages used for spell checking.

```csharp
ILanguages Languages { get; }
```

##### Property Value

 [ILanguages](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ILanguages)

##### Remarks

<p>
    On Linux and Windows the dictionaries for spell checking are downloaded
    programmatically and stored in the user data directory.
</p>
<p>
    On macOS returns the languages for spell checking configured in the system settings.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.SpellCheck.ISpellChecker" data-throw-if-not-resolved="false"></xref> has already been disposed.
