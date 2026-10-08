
# User data profiles

**Lead**
This guide describes how to save, update and manage user data such as name, address, email etc. entered in webforms.


## Overview

Chromium has built-in functionality that allows remembering the user data entered into web forms. When the user submits a web form containing this data then the library will ask whether to save it to the user data store.

If you save it, the next time you load the form, the library will suggest you to autofill it.

![Address](https://teamdev.com/dotnetbrowser/img/releases/2-14/address.webp)

To access and manage the saved data, use `IUserDataProfileStore`:


**C#**
```csharp
IReadOnlyList<UserDataProfile> allUserDataProfiles = 
    Engine.Profiles.Default.UserDataProfileStore.All;
```

**VB**
```vb
Dim allUserDataProfiles As IReadOnlyList(Of UserDataProfile) = 
    Engine.Profiles.Default.UserDataProfileStore.All
```



## Saving user data

When the user submits a form containing the user data such as city, street, zip code, email address, phone number, etc., the library will ask you if you would like to save this data via `SaveUserDataProfileHandler`. In the handler, you will be prompted to save or decline. For example:


**C#**
```csharp
Browser.UserDataProfiles.SaveUserDataProfileHandler
    = new Handler<SaveUserDataProfileParameters, SaveUserDataProfileResponse>(
        p => SaveUserDataProfileResponse.Save);
```

**VB**
```vb
Browser.UserDataProfiles.SaveUserDataProfileHandler = 
    New Handler(Of SaveUserDataProfileParameters, SaveUserDataProfileResponse)
        (Function(p) SaveUserDataProfileResponse.Save)
```



If you choose to save, then this user data will be added to the user data store. Next time you enter the same user data to the form the handler will not be invoked.

If you choose to decline to save the user data, then it will not be added to the store and next time when entering the exact same user data the handler will be invoked again.

## Updating user data

When the user submits the web form with updated user data, the library will ask you to update it in the user data store via `UpdateUserDataProfileHandler`. In this handler, you will be prompted to update or decline the user data in UserDataProfiles. For example:


**C#**
```csharp
Browser.UserDataProfiles.UpdateUserDataProfileHandler
    = new Handler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse>(
        p => UpdateUserDataProfileResponse.Update);
```

**VB**
```vb
Browser.UserDataProfiles.UpdateUserDataProfileHandler = 
    New Handler(Of UpdateUserDataProfileParameters, UpdateUserDataProfileResponse)
        (Function(p) UpdateUserDataProfileResponse.Update)
```



## Managing user data

Each record in the user data store is represented by a separate instance of `UserDataProfile`. It contains a city, state, street, zip code, email address, full name, etc.

To get all records, use:


**C#**
```csharp
IReadOnlyList<UserDataProfile> allUserDataProfiles = 
    Engine.Profiles.Default.UserDataProfileStore.All;
```

**VB**
```vb
Dim allUserDataProfiles As IReadOnlyList(Of UserDataProfile) = 
    Engine.Profiles.Default.UserDataProfileStore.All
```



To remove any record, use:


**C#**
```csharp
Engine.Profiles.Default.UserDataProfileStore.Remove(userDataProfile);
```

**VB**
```vb
Engine.Profiles.Default.UserDataProfileStore.Remove(userDataProfile)
```



To clear all user data profiles, use the following method:


**C#**
```csharp
Engine.Profiles.Default.UserDataProfileStore.Clear();
```

**VB**
```vb
Engine.Profiles.Default.UserDataProfileStore.Clear()
```


