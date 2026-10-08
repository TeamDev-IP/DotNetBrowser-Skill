# <a id="DotNetBrowser_Profile_IProfiles"></a> Interface IProfiles

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The collection of the Chromium profiles.

```csharp
public interface IProfiles : IEnumerable<IProfile>, IEnumerable, IAutoDisposable
```

#### Implements

[IEnumerable<IProfile\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Profile_IProfiles_Count"></a> Count

Gets the current number of profiles.

```csharp
int Count { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Profile_IProfiles_Default"></a> Default

Gets the default profile used by the Chromium engine.

```csharp
IProfile Default { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Profile_IProfiles_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

## Methods

### <a id="DotNetBrowser_Profile_IProfiles_Create_System_String_DotNetBrowser_Profile_ProfileType_"></a> Create\(string, ProfileType\)

Creates a new Chromium profile of the specified <code class="paramref">profileType</code> with the specified
<code class="paramref">name</code>.

```csharp
IProfile Create(string name, ProfileType profileType = ProfileType.Regular)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The profile name. Cannot be null or empty.

`profileType` [ProfileType](DotNetBrowser.Profile.ProfileType.md)

The profile type. If omitted, the regular profile will be created.

#### Returns

 [IProfile](DotNetBrowser.Profile.IProfile.md)

The new Chromium profile.

### <a id="DotNetBrowser_Profile_IProfiles_Remove_DotNetBrowser_Profile_IProfile_"></a> Remove\(IProfile\)

Removes the existing Chromium profile.

```csharp
bool Remove(IProfile profile)
```

#### Parameters

`profile` [IProfile](DotNetBrowser.Profile.IProfile.md)

The Chromium profile to remove

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the profile was removed, <code>false</code> otherwise.

#### Remarks

When the profile is removed, the corresponding <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instances are disposed.
The downloads in progress are canceled, and the profile directory is scheduled for deletion.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The profile belongs to a different IEngine instance.

