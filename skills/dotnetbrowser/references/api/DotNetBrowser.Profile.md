# <a id="DotNetBrowser_Profile"></a> Namespace DotNetBrowser.Profile

### Interfaces

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

The Chromium profile.

 [IProfilePreferences](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfilePreferences)

The preferences of a <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref>.

 [IProfiles](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfiles)

The collection of the Chromium profiles.

### Enums

 [CookieControlsMode](DotNetBrowser.Profile.md#DotNetBrowser_Profile_CookieControlsMode)

The Chromium third-party cookies block mode.

 [ProfileType](DotNetBrowser.Profile.md#DotNetBrowser_Profile_ProfileType)

The Chromium profile type.

## <a id="DotNetBrowser_Profile_IProfile"></a> Interface IProfile

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The Chromium profile.

```csharp
public interface IProfile : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Profile_IProfile_CookieStore"></a> CookieStore

Gets the cookie service that allows managing cookies.

```csharp
ICookieStore CookieStore { get; }
```

##### Property Value

 [ICookieStore](DotNetBrowser.Cookies.md#DotNetBrowser_Cookies_ICookieStore)

#### <a id="DotNetBrowser_Profile_IProfile_CreditCardStore"></a> CreditCardStore

Gets the service that allows working with the credit card store.

```csharp
ICreditCardStore CreditCardStore { get; }
```

##### Property Value

 [ICreditCardStore](DotNetBrowser.Card.md#DotNetBrowser_Card_ICreditCardStore)

#### <a id="DotNetBrowser_Profile_IProfile_Downloads"></a> Downloads

Gets the service that allows managing downloads.

```csharp
IDownloads Downloads { get; }
```

##### Property Value

 [IDownloads](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_IDownloads)

#### <a id="DotNetBrowser_Profile_IProfile_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Profile_IProfile_Extensions"></a> Extensions

Gets the service that allows managing extensions.

```csharp
IExtensions Extensions { get; }
```

##### Property Value

 [IExtensions](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensions)

#### <a id="DotNetBrowser_Profile_IProfile_HttpAuthCache"></a> HttpAuthCache

Gets the HTTP Authentication cache service, which is responsible for storing
HTTP authentication identities and challenge info

```csharp
IHttpAuthCache HttpAuthCache { get; }
```

##### Property Value

 [IHttpAuthCache](DotNetBrowser.Cache.md#DotNetBrowser_Cache_IHttpAuthCache)

#### <a id="DotNetBrowser_Profile_IProfile_HttpCache"></a> HttpCache

Gets the HTTP cache service.

```csharp
IHttpCache HttpCache { get; }
```

##### Property Value

 [IHttpCache](DotNetBrowser.Cache.md#DotNetBrowser_Cache_IHttpCache)

#### <a id="DotNetBrowser_Profile_IProfile_IsDefault"></a> IsDefault

Indicates whether this profile is default.

```csharp
bool IsDefault { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Profile_IProfile_MediaCasting"></a> MediaCasting

Gets the service that allows working with media casting.

```csharp
IMediaCasting MediaCasting { get; }
```

##### Property Value

 [IMediaCasting](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaCasting)

#### <a id="DotNetBrowser_Profile_IProfile_Name"></a> Name

Gets the profile name.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Profile_IProfile_Network"></a> Network

Gets the service that allows working with network.

```csharp
INetwork Network { get; }
```

##### Property Value

 [INetwork](DotNetBrowser.Net.md#DotNetBrowser_Net_INetwork)

#### <a id="DotNetBrowser_Profile_IProfile_PasswordStore"></a> PasswordStore

Gets the service that allows working with the password store.

```csharp
IPasswordStore PasswordStore { get; }
```

##### Property Value

 [IPasswordStore](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_IPasswordStore)

#### <a id="DotNetBrowser_Profile_IProfile_Path"></a> Path

Gets the profile path.

```csharp
string Path { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Profile_IProfile_Permissions"></a> Permissions

Gets the service that allows managing permissions.

```csharp
IPermissions Permissions { get; }
```

##### Property Value

 [IPermissions](DotNetBrowser.Permissions.md#DotNetBrowser_Permissions_IPermissions)

#### <a id="DotNetBrowser_Profile_IProfile_Plugins"></a> Plugins

Gets the service that allows configuring plugins.

```csharp
IPlugins Plugins { get; }
```

##### Property Value

 [IPlugins](DotNetBrowser.Plugins.md#DotNetBrowser_Plugins_IPlugins)

#### <a id="DotNetBrowser_Profile_IProfile_Preferences"></a> Preferences

Gets the profile preferences.

```csharp
IProfilePreferences Preferences { get; }
```

##### Property Value

 [IProfilePreferences](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfilePreferences)

#### <a id="DotNetBrowser_Profile_IProfile_Proxy"></a> Proxy

Gets the service that allows working with proxy.

```csharp
IProxy Proxy { get; }
```

##### Property Value

 [IProxy](DotNetBrowser.Net.Proxy.md#DotNetBrowser_Net_Proxy_IProxy)

#### <a id="DotNetBrowser_Profile_IProfile_SpellChecker"></a> SpellChecker

Gets the service that allows working with spell checking functionality.

```csharp
ISpellChecker SpellChecker { get; }
```

##### Property Value

 [ISpellChecker](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_ISpellChecker)

#### <a id="DotNetBrowser_Profile_IProfile_Type"></a> Type

Gets the profile type.

```csharp
ProfileType Type { get; }
```

##### Property Value

 [ProfileType](DotNetBrowser.Profile.md#DotNetBrowser_Profile_ProfileType)

#### <a id="DotNetBrowser_Profile_IProfile_UserAgentMetadata"></a> UserAgentMetadata

Gets the default user-agent metadata (client hints).

```csharp
UserAgentMetadata UserAgentMetadata { get; }
```

##### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Profile_IProfile_UserDataProfileStore"></a> UserDataProfileStore

Gets the service that allows working with the user date profile store.

```csharp
IUserDataProfileStore UserDataProfileStore { get; }
```

##### Property Value

 [IUserDataProfileStore](DotNetBrowser.UserData.md#DotNetBrowser_UserData_IUserDataProfileStore)

#### <a id="DotNetBrowser_Profile_IProfile_ZoomLevels"></a> ZoomLevels

Gets the service that allows working with zoom.

```csharp
IZoomLevels ZoomLevels { get; }
```

##### Property Value

 [IZoomLevels](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_IZoomLevels)

### Methods

#### <a id="DotNetBrowser_Profile_IProfile_ClearAllData"></a> ClearAllData\(\)

Clears all browsing data for this profile, including cache, cookies, history, and other stored data.

```csharp
Task ClearAllData()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous operation.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Profile_IProfile_CreateBrowser"></a> CreateBrowser\(\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page.

```csharp
IBrowser CreateBrowser()
```

##### Returns

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Profile_IProfile_CreateBrowser_DotNetBrowser_Engine_RenderingMode_"></a> CreateBrowser\(RenderingMode\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page
and the specified rendering mode.

```csharp
IBrowser CreateBrowser(RenderingMode renderingMode)
```

##### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

the rendering mode to use for this browser instance.

##### Returns

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Profile_IProfilePreferences"></a> Interface IProfilePreferences

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The preferences of a <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IProfilePreferences : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Profile_IProfilePreferences_AutofillEnabled"></a> AutofillEnabled

Enables or disables the web form autofill and displaying of suggestions pop-ups. By default, the autofill is
enabled.

```csharp
bool AutofillEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

<p>
    <b>Important:</b> the autofill for the <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> passwords is always
    enabled except the cases when a site has an invalid SSL certificate or the scheme is not
    registered as web-safe.The list of web-safe schemes: HTTP, HTTPS, WS, and WSS.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Profile_IProfilePreferences_CaretBrowsingEnabled"></a> CaretBrowsingEnabled

Enables or disables the caret browsing. By default, the caret browsing is
disabled.

```csharp
bool CaretBrowsingEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Profile_IProfilePreferences_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Profile_IProfilePreferences_NetworkPredictionEnabled"></a> NetworkPredictionEnabled

Enables or disables the network prediction. By default, the network prediction is enabled.

```csharp
bool NetworkPredictionEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

Network prediction is the built-in feature of Chromium that allows you to open the most visited websites faster.
This is done by DNS prefetching, TCP and SSL preconnection, prerendering of web pages, and resource prefetching.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Profile_IProfilePreferences_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Profile_IProfilePreferences_ThirdPartyCookieMode"></a> ThirdPartyCookieMode

Gets or sets the third-party cookies blocking mode.

```csharp
CookieControlsMode ThirdPartyCookieMode { get; set; }
```

##### Property Value

 [CookieControlsMode](DotNetBrowser.Profile.md#DotNetBrowser_Profile_CookieControlsMode)

## <a id="DotNetBrowser_Profile_IProfiles"></a> Interface IProfiles

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The collection of the Chromium profiles.

```csharp
public interface IProfiles : IEnumerable<IProfile>, IEnumerable, IAutoDisposable
```

##### Implements

[IEnumerable<IProfile\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Profile_IProfiles_Count"></a> Count

Gets the current number of profiles.

```csharp
int Count { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Profile_IProfiles_Default"></a> Default

Gets the default profile used by the Chromium engine.

```csharp
IProfile Default { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Profile_IProfiles_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

### Methods

#### <a id="DotNetBrowser_Profile_IProfiles_Create_System_String_DotNetBrowser_Profile_ProfileType_"></a> Create\(string, ProfileType\)

Creates a new Chromium profile of the specified <code class="paramref">profileType</code> with the specified
<code class="paramref">name</code>.

```csharp
IProfile Create(string name, ProfileType profileType = ProfileType.Regular)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The profile name. Cannot be null or empty.

`profileType` [ProfileType](DotNetBrowser.Profile.md#DotNetBrowser_Profile_ProfileType)

The profile type. If omitted, the regular profile will be created.

##### Returns

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

The new Chromium profile.

#### <a id="DotNetBrowser_Profile_IProfiles_Remove_DotNetBrowser_Profile_IProfile_"></a> Remove\(IProfile\)

Removes the existing Chromium profile.

```csharp
bool Remove(IProfile profile)
```

##### Parameters

`profile` [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

The Chromium profile to remove

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the profile was removed, <code>false</code> otherwise.

##### Remarks

When the profile is removed, the corresponding <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instances are disposed.
The downloads in progress are canceled, and the profile directory is scheduled for deletion.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The profile belongs to a different IEngine instance.

## <a id="DotNetBrowser_Profile_CookieControlsMode"></a> Enum CookieControlsMode

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The Chromium third-party cookies block mode.

```csharp
public enum CookieControlsMode
```

### Fields

`BlockThirdParty = 2` 

Sites can't use user cookies to see user browsing activity across different sites, for example, to personalize ads.
Features on some sites may not work.



`IncognitoOnly = 3` 

While in Incognito, sites can't use user cookies to see user browsing activity across sites, even related sites.
The user browsing activity isn't used for things like personalizing ads. Features on some sites may not work.



`Off = 1` 

Sites can use cookies to see the user browsing activity across different sites, for example, to personalize ads.



`Undefined = 0` 

Reserved value.

## <a id="DotNetBrowser_Profile_ProfileType"></a> Enum ProfileType

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The Chromium profile type.

```csharp
public enum ProfileType
```

### Fields

`Incognito = 1` 

The incognito Chromium profile.



`Regular = 0` 

The regular Chromium profile.
