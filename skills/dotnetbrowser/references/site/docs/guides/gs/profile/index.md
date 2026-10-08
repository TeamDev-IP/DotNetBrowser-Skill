
# Profile

**Lead**
This guide describes how to manage Chromium profiles.


## Overview

Profile stores the user data such as navigation history, cookies, cache, passwords, etc.

In DotNetBrowser the profile-related functionality can be accessed via `IEngine.Profiles` property which returns `IProfiles`. This interface allows managing profiles. 

Each profile is represented by the separate `IProfile` instance. Using this instance you can get all necessary information about the profile like its name, absolute path to the directory where profile stores its data, and provides access to profile-related services:

- `ZoomLevels`
- `Plugins`
- `Proxy`
- `Network`
- `SpellChecker`
- `CookieStore`
- `HttpCache`
- `Downloads`
- `Permissions`

## Default profile

When you create an `IEngine` instance, the default profile is always initialized. You can obtain it using the `IProfiles.Default` property:


**C#**
```csharp
IProfile defaultProfile = engine.Profiles.Default;
```

**VB**
```vb
Dim defaultProfile As IProfile = engine.Profiles.Default
```



### Incognito

To make the default profile incognito, use the [Incognito](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#incognito) option when creating an `Engine` instance. This option affects the default profile only.

## Creating profile

To create a new profile, use the `IProfiles.Create()` method.


**C#**
```csharp
IProfile profile = engine.Profiles.Create("Test");
```

**VB**
```vb
Dim profile As IProfile = engine.Profiles.Create("Test")
```



Profile stores its data such as navigation history, proxy settings, cookies, spellchecker configurations, etc. in a separate directory inside the [user data directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory).

## Creating Incognito profile

To create an incognito profile, the `ProfileType.Incognito` parameter should be used.


**C#**
```csharp
IProfile newIncognitoProfile = engine.Profiles.Create("Test", ProfileType.Incognito);
```

**VB**
```vb
Dim newIncognitoProfile As IProfile = engine.Profiles.Create("Test", ProfileType.Incognito)
```



## Getting profiles

To access all profiles created in the engine, use `IProfiles` as `IEnumerable<IProfile>`:


**C#**
```csharp
foreach (IProfile profile in profiles)
{
    string name = profile.Name;
}
```

**VB**
```vb
For Each profile As IProfile In profiles
    Dim name As String = profile.Name
Next
```



**Note**
This approach will also iterate over the default profile.
 

## Removing profile

To remove an existing profile you should use the `IProfiles.Remove(IProfile)` method.

When you remove a profile, all browsers associated with it will be disposed. An attempt to use an already removed `IProfile` instance will lead to the `ObjectDisposedException`.

**Important**
The default profile cannot be removed. If you pass the default profile to `IProfiles.Remove(IProfile)`, the method does not remove it and returns `false`.


## Clearing profile data

To clean a profile data, use the IProfile.ClearAllData() method.

**C#**
```csharp
engine.Profiles.Default.ClearAllData();
```

**VB**
```vb
engine.Profiles.Default.ClearAllData()
```



The method removes cache, cookies, browsing history, and other stored profile data.