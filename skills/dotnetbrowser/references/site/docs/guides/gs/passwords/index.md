
# Passwords

**Lead**
This guide describes how to save, update, and manage passwords the user enters in a new form online.


## Overview

Chromium has a built-in functionality that allows remembering the entered credentials when the user submits a new form containing username and password. The library will ask you if you’d like to save the credentials.

If you save them, the next time you load the form, the library will suggest autofill it.

![Password autofill](https://teamdev.com/dotnetbrowser/img/articles/guides/passwords/autofill.webp)

## Saving passwords

When the user submits a new form containing a username and password, the `SavePasswordHandler` will be called. In the handler, you can decide whether to save the credentials for this website by returning the "Save" or "Never" option. For example:


**C#**
```csharp
Browser.Passwords.SavePasswordHandler = 
    new Handler<SavePasswordParameters, SavePasswordResponse>(p =>
    {
        return SavePasswordResponse.Save;
    });
```

**VB**
```vb
Browser.Passwords.SavePasswordHandler = 
    New Handler(Of SavePasswordParameters, SavePasswordResponse)(Function(p)
        Return SavePasswordResponse.Save
    End Function)
```



If you choose to save the password, it will be added to the password store. If you select the "Never" option, the library will not suggest saving the passwords for this web page anymore.

## Updating passwords

When the user submits the previously submitted form with the same username and a new password, the `UpdatePasswordHandler` will be called. In this handler, you can decide whether to update the existing credentials or ignore the new value. For example:


**C#**
```csharp
Browser.Passwords.UpdatePasswordHandler = 
    new Handler<UpdatePasswordParameters, UpdatePasswordResponse>(p =>
    {
        return UpdatePasswordResponse.Update;
    });
```

**VB**
```vb
Browser.Passwords.UpdatePasswordHandler = 
    New Handler(Of UpdatePasswordParameters, UpdatePasswordResponse)(Function(p)
        Return UpdatePasswordResponse.Update
    End Function)
```



## Managing passwords

Each element in the password store is represented by a `PasswordRecord` instance. It contains the user’s login and the URL of a web page where the form was submitted. It doesn’t contain the password itself.

To read all saved and blocklisted records, use:


**C#**
```csharp
IReadOnlyList<PasswordRecord> allPasswords = 
    Engine.Profiles.Default.PasswordStore.All;
```

**VB**
```vb
Dim allPasswords As IReadOnlyList(Of PasswordRecord) = 
    Engine.Profiles.Default.PasswordStore.All
```



To read only saved records, use:


**C#**
```csharp
IReadOnlyList<PasswordRecord> savedPasswords = 
    Engine.Profiles.Default.PasswordStore.AllSaved;
```

**VB**
```vb
Dim savedPasswords As IReadOnlyList(Of PasswordRecord) = 
    Engine.Profiles.Default.PasswordStore.AllSaved
```



For saved records, `PasswordRecord.Url` contains the full form URL
(for example, `https://example.com/login`).

To read only the records with the websites for which the passwords will never be saved, use:


**C#**
```csharp
IReadOnlyList<PasswordRecord> neverSavedPasswords = 
    Engine.Profiles.Default.PasswordStore.AllNeverSaved;
```

**VB**
```vb
Dim neverSavedPasswords As IReadOnlyList(Of PasswordRecord) = 
    Engine.Profiles.Default.PasswordStore.AllNeverSaved
```



For never-saved records, `PasswordRecord.Url` contains the origin URL
(for example, `https://example.com/`).

To remove all records from the store use:


**C#**
```csharp
PasswordStore.Clear();
```

**VB**
```vb
PasswordStore.Clear()
```



To remove one specific record from the store, use:


**C#**
```csharp
var passwordStore = Engine.Profiles.Default.PasswordStore;
PasswordRecord record = passwordStore.AllSaved
    .First(r => r.Url.StartsWith("https://example.com"));
passwordStore.Remove(record);
```

**VB**
```vb
Dim passwordStore = Engine.Profiles.Default.PasswordStore
Dim record As PasswordRecord = passwordStore.AllSaved.
    First(Function(r) r.Url.StartsWith("https://example.com"))

passwordStore.Remove(record)
```



To remove records associated with a specific URL, use the
`RemoveByUrl(...)` extension method:


**C#**
```csharp
PasswordStore.RemoveByUrl(url);
```

**VB**
```vb
PasswordStore.RemoveByUrl(url)
```


