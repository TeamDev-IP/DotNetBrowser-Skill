# <a id="DotNetBrowser_SpellCheck_SpellCheckMenu"></a> Class SpellCheckMenu

Namespace: [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)  
Assembly: DotNetBrowser.dll  

A spell check menu in the context menu.

```csharp
public sealed class SpellCheckMenu
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SpellCheckMenu](DotNetBrowser.SpellCheck.SpellCheckMenu.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_AddToDictionaryMenuItemText"></a> AddToDictionaryMenuItemText

Gets the localized text of the "Add to Dictionary" menu item.

```csharp
public string AddToDictionaryMenuItemText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_DictionarySuggestions"></a> DictionarySuggestions

Gets a collection of the suggested replacements for a misspelled word under the cursor.

```csharp
public IEnumerable<string> DictionarySuggestions { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

### <a id="DotNetBrowser_SpellCheck_SpellCheckMenu_MisspelledWord"></a> MisspelledWord

Gets the misspelled word under the cursor, if any.

```csharp
public string MisspelledWord { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

