# <a id="DotNetBrowser_Profile_IProfile"></a> Interface IProfile

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The Chromium profile.

```csharp
public interface IProfile : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Profile_IProfile_CookieStore"></a> CookieStore

Gets the cookie service that allows managing cookies.

```csharp
ICookieStore CookieStore { get; }
```

#### Property Value

 [ICookieStore](DotNetBrowser.Cookies.ICookieStore.md)

### <a id="DotNetBrowser_Profile_IProfile_CreditCardStore"></a> CreditCardStore

Gets the service that allows working with the credit card store.

```csharp
ICreditCardStore CreditCardStore { get; }
```

#### Property Value

 [ICreditCardStore](DotNetBrowser.Card.ICreditCardStore.md)

### <a id="DotNetBrowser_Profile_IProfile_Downloads"></a> Downloads

Gets the service that allows managing downloads.

```csharp
IDownloads Downloads { get; }
```

#### Property Value

 [IDownloads](DotNetBrowser.Downloads.IDownloads.md)

### <a id="DotNetBrowser_Profile_IProfile_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Profile_IProfile_Extensions"></a> Extensions

Gets the service that allows managing extensions.

```csharp
IExtensions Extensions { get; }
```

#### Property Value

 [IExtensions](DotNetBrowser.Extensions.IExtensions.md)

### <a id="DotNetBrowser_Profile_IProfile_HttpAuthCache"></a> HttpAuthCache

Gets the HTTP Authentication cache service, which is responsible for storing
HTTP authentication identities and challenge info

```csharp
IHttpAuthCache HttpAuthCache { get; }
```

#### Property Value

 [IHttpAuthCache](DotNetBrowser.Cache.IHttpAuthCache.md)

### <a id="DotNetBrowser_Profile_IProfile_HttpCache"></a> HttpCache

Gets the HTTP cache service.

```csharp
IHttpCache HttpCache { get; }
```

#### Property Value

 [IHttpCache](DotNetBrowser.Cache.IHttpCache.md)

### <a id="DotNetBrowser_Profile_IProfile_IsDefault"></a> IsDefault

Indicates whether this profile is default.

```csharp
bool IsDefault { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Profile_IProfile_MediaCasting"></a> MediaCasting

Gets the service that allows working with media casting.

```csharp
IMediaCasting MediaCasting { get; }
```

#### Property Value

 [IMediaCasting](DotNetBrowser.Cast.IMediaCasting.md)

### <a id="DotNetBrowser_Profile_IProfile_Name"></a> Name

Gets the profile name.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Profile_IProfile_Network"></a> Network

Gets the service that allows working with network.

```csharp
INetwork Network { get; }
```

#### Property Value

 [INetwork](DotNetBrowser.Net.INetwork.md)

### <a id="DotNetBrowser_Profile_IProfile_PasswordStore"></a> PasswordStore

Gets the service that allows working with the password store.

```csharp
IPasswordStore PasswordStore { get; }
```

#### Property Value

 [IPasswordStore](DotNetBrowser.Passwords.IPasswordStore.md)

### <a id="DotNetBrowser_Profile_IProfile_Path"></a> Path

Gets the profile path.

```csharp
string Path { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Profile_IProfile_Permissions"></a> Permissions

Gets the service that allows managing permissions.

```csharp
IPermissions Permissions { get; }
```

#### Property Value

 [IPermissions](DotNetBrowser.Permissions.IPermissions.md)

### <a id="DotNetBrowser_Profile_IProfile_Plugins"></a> Plugins

Gets the service that allows configuring plugins.

```csharp
IPlugins Plugins { get; }
```

#### Property Value

 [IPlugins](DotNetBrowser.Plugins.IPlugins.md)

### <a id="DotNetBrowser_Profile_IProfile_Preferences"></a> Preferences

Gets the profile preferences.

```csharp
IProfilePreferences Preferences { get; }
```

#### Property Value

 [IProfilePreferences](DotNetBrowser.Profile.IProfilePreferences.md)

### <a id="DotNetBrowser_Profile_IProfile_Proxy"></a> Proxy

Gets the service that allows working with proxy.

```csharp
IProxy Proxy { get; }
```

#### Property Value

 [IProxy](DotNetBrowser.Net.Proxy.IProxy.md)

### <a id="DotNetBrowser_Profile_IProfile_SpellChecker"></a> SpellChecker

Gets the service that allows working with spell checking functionality.

```csharp
ISpellChecker SpellChecker { get; }
```

#### Property Value

 [ISpellChecker](DotNetBrowser.SpellCheck.ISpellChecker.md)

### <a id="DotNetBrowser_Profile_IProfile_Type"></a> Type

Gets the profile type.

```csharp
ProfileType Type { get; }
```

#### Property Value

 [ProfileType](DotNetBrowser.Profile.ProfileType.md)

### <a id="DotNetBrowser_Profile_IProfile_UserAgentMetadata"></a> UserAgentMetadata

Gets the default user-agent metadata (client hints).

```csharp
UserAgentMetadata UserAgentMetadata { get; }
```

#### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Profile_IProfile_UserDataProfileStore"></a> UserDataProfileStore

Gets the service that allows working with the user date profile store.

```csharp
IUserDataProfileStore UserDataProfileStore { get; }
```

#### Property Value

 [IUserDataProfileStore](DotNetBrowser.UserData.IUserDataProfileStore.md)

### <a id="DotNetBrowser_Profile_IProfile_ZoomLevels"></a> ZoomLevels

Gets the service that allows working with zoom.

```csharp
IZoomLevels ZoomLevels { get; }
```

#### Property Value

 [IZoomLevels](DotNetBrowser.Zoom.IZoomLevels.md)

## Methods

### <a id="DotNetBrowser_Profile_IProfile_ClearAllData"></a> ClearAllData\(\)

Clears all browsing data for this profile, including cache, cookies, history, and other stored data.

```csharp
Task ClearAllData()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous operation.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Profile_IProfile_CreateBrowser"></a> CreateBrowser\(\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page.

```csharp
IBrowser CreateBrowser()
```

#### Returns

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Profile_IProfile_CreateBrowser_DotNetBrowser_Engine_RenderingMode_"></a> CreateBrowser\(RenderingMode\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page
and the specified rendering mode.

```csharp
IBrowser CreateBrowser(RenderingMode renderingMode)
```

#### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

the rendering mode to use for this browser instance.

#### Returns

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

