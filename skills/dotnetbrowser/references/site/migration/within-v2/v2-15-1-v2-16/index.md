
# Migrating from 2.15.1 to 2.16

**Lead**
In this migration guide we describe the changes in the API between versions 2.15.1 and 2.16.


## Removed API

### Credit card

**v2.16**

The `CreditCardNetworkType.Google` has been removed.


### Cache

**v2.15.1**

To clear the HTTP cache and perform an action after completion, the following code is used:

```csharp
engine.HttpCache.ClearDiskCache().ContinueWith(t => 
{
    // Cache has been cleared.
});
```

**v2.16**

The obsolete `IHttpCache.ClearDiskCache()` method has been removed. Now the `IHttpCache.Clear()` method is used to clear the HTTP cache associated with a certain profile:

```csharp
profile.HttpCache.Clear().ContinueWith(t => 
{
    // Cache has been cleared.
});
```

### Network

**v2.16**

The `Url` propertty is no longer available in the `CanAccessFileParameters` used by `INetwork.CanAccessFileHandler`.

## Updated API

### Password store

**v2.15.1**

`PasswordStore` property represents a string that specifies which encryption storage backend to use:

```csharp
EngineOptions options = new EngineOptions.Builder()
{
    PasswordStore = "gnome-keyring"
}.Build();
```

**v2.16**

Now you can specify the required encryption storage from the list:

```csharp
EngineOptions options = new EngineOptions.Builder()
{
    PasswordStore = PasswordStore.GnomeKeyring
}.Build();
```

### Spellchecker

#### Configuring languages

**v2.15.1**

To configure the spell checker with the required dictionaries, use the `ISpellChecker.DictionaryNames` property. Chromium downloads the dictionary files automatically from its web servers.

```csharp
spellChecker.DictionaryNames = new List<string>{"en-US", "de"};
```

**v2.16**

There are two new methods to manage languages in `SpellChecker` service:

```csharp
spellChecker.Languages.Add(Language.EnglishUs);
spellChecker.Languages.Remove(Language.EnglishUs);
```

The `addLaspellChecker.Languages.Add()` method downloads the dictionaries and blocks the current thread until they are loaded.

The `spellChecker.Languages.Remove()` method excludes the language from the spellchecking.

#### Getting languages

**v2.15.1**

To get the list of dictionaries used for spellchecking, use the `dictionaryNames` property:

```csharp
IReadOnlyList<Language> languages = spellChecker.dictionaryNames();
```

**v2.16**

To get the list of spellcheck languages, use the following approach:

```csharp
ISpellChecker spellChecker = Engine.Profiles.Default.SpellChecker;
IReadOnlyList<Language> languages = spellChecker.Languages.All;
```
