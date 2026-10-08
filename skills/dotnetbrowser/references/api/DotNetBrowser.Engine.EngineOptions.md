# <a id="DotNetBrowser_Engine_EngineOptions"></a> Class EngineOptions

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The options that are used to configure <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

```csharp
public class EngineOptions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Engine_EngineOptions_BinariesExtractionOptions"></a> BinariesExtractionOptions

Gets the options that are used to configure the Chromium binaries extraction process.

```csharp
public BinariesExtractionOptions BinariesExtractionOptions { get; }
```

#### Property Value

 [BinariesExtractionOptions](DotNetBrowser.Engine.BinariesExtractionOptions.md)

### <a id="DotNetBrowser_Engine_EngineOptions_ChromiumDirectory"></a> ChromiumDirectory

Gets the absolute path to the directory where the Chromium binaries are located.

```csharp
public string ChromiumDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    If the directory contains the Chromium binaries, the library will check them and make
    sure that they are compatible with the current library version. If the directory does not
    contain the Chromium binaries, or the binaries aren't compatible with the current library
    version, the library will search for the binaries inside the assemblies from the application
    references and working directory and extract them into the given directory programmatically.
    It might take some time to extract the Chromium binaries from a JAR archive. The time depends on the hardware
    (CPU and SSD/HDD) performance.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_ChromiumSwitches"></a> ChromiumSwitches

Gets an immutable collection of the Chromium switches that will be passed to the Chromium Main
process.

```csharp
public IEnumerable<string> ChromiumSwitches { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Remarks

<p>
    The library does not support all the possible Chromium switches, so there is no guarantee
    that the passed switches will work. The switches from this list will overwrite the
    corresponding options configured through the <xref href="DotNetBrowser.Engine.EngineOptions.Builder" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    For example, if you configure the remote debugging port using the<xref href="DotNetBrowser.Engine.EngineOptions.RemoteDebuggingPort" data-throw-if-not-resolved="false"></xref>
    property and then add the <code>--remote-debugging-port</code> switch using the
    <xref href="DotNetBrowser.Engine.EngineOptions.ChromiumSwitches" data-throw-if-not-resolved="false"></xref> property, then the port from the switch will
    be used.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_CrashDumpDirectory"></a> CrashDumpDirectory

Gets the path that will be used to store the automatically generated Chromium crash dumps.

```csharp
public string CrashDumpDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Engine_EngineOptions_DiskCacheSize"></a> DiskCacheSize

Gets the disk cache size.

```csharp
public long DiskCacheSize { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### Remarks

If the disk cache size was not set, then it will be calculated automatically. The size
depends on the available disk space in the volume where the disk cache is located.

### <a id="DotNetBrowser_Engine_EngineOptions_GoogleApiKey"></a> GoogleApiKey

Gets the Google API key.

```csharp
public string GoogleApiKey { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_GoogleDefaultClientId"></a> GoogleDefaultClientId

Gets the Google client ID.

```csharp
public string GoogleDefaultClientId { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_GoogleDefaultClientSecret"></a> GoogleDefaultClientSecret

Gets the Google client secret.

```csharp
public string GoogleDefaultClientSecret { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_IsAutoplayEnabled"></a> IsAutoplayEnabled

Indicates whether video playback will automatically start after page loading.

```csharp
public bool IsAutoplayEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsDnsOverHttpsDisabled"></a> IsDnsOverHttpsDisabled

Indicates whether the DNS over HTTPS (DoH) protocol is disabled.

```csharp
public bool IsDnsOverHttpsDisabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsFileAccessFromFilesAllowed"></a> IsFileAccessFromFilesAllowed

Indicates whether file access from files is allowed.

```csharp
public bool IsFileAccessFromFilesAllowed { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsGpuDisabled"></a> IsGpuDisabled

Indicates whether GPU is disabled.

```csharp
public bool IsGpuDisabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsIncognitoEnabled"></a> IsIncognitoEnabled

Indicates whether the incognito mode for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance is enabled.

```csharp
public bool IsIncognitoEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

In the incognito mode the user data such as browsing history, cookies, site data, and the
information entered in forms are stored in memory and released once you close the <code>Engine</code>.

### <a id="DotNetBrowser_Engine_EngineOptions_IsMediaRoutingEnabled"></a> IsMediaRoutingEnabled

Indicates whether media routing is enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

<p>
    By default, it is disabled.
</p>

```csharp
public bool IsMediaRoutingEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsNativeKeyboardInputEnabled"></a> IsNativeKeyboardInputEnabled

Indicates whether the keyboard events processing using native system API is enabled.

<p>
    When not applied, the .NET keyboard listeners is used to collect key events, pre-handle them
    and dispatch to Chromium.
</p>
<p>
    When applied, the OS-specific API is used to collect key events from .NET with subsequent
    dispatch to Chromium.
</p>

```csharp
public bool IsNativeKeyboardInputEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsSandboxDisabled"></a> IsSandboxDisabled

Indicates whether the sandbox is disabled.

```csharp
public bool IsSandboxDisabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsTouchMenuDisabled"></a> IsTouchMenuDisabled

Indicates whether touch popup menu is disabled.

```csharp
public bool IsTouchMenuDisabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_IsWebSecurityDisabled"></a> IsWebSecurityDisabled

Indicates whether the same-origin policy is disabled.

```csharp
public bool IsWebSecurityDisabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Language"></a> Language

Gets the Chromium language that is used on the default error pages and message dialogs.

```csharp
public Language Language { get; }
```

#### Property Value

 [Language](DotNetBrowser.Ui.Language.md)

#### Remarks

<p>
    By default, the language is dynamically configured according to the default locale of the
    application. If the list of supported languages does not contain the language obtained from
    the application locale, then the US English language is used.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_LicenseKey"></a> LicenseKey

Gets the license key.

```csharp
public string LicenseKey { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

The license key can be set via adding the "dotnetbrowser.license" file as embedded resource or individually
for every <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> using the <xref href="DotNetBrowser.Engine.EngineOptions.LicenseKey" data-throw-if-not-resolved="false"></xref> property.

### <a id="DotNetBrowser_Engine_EngineOptions_PasswordStore"></a> PasswordStore

Gets the password store type which specifies the
storage backend should be used to encrypt cookies on Linux.

```csharp
public PasswordStore PasswordStore { get; }
```

#### Property Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

#### Remarks

If the password store type was not set, then the encryption storage backend is chosen by
Chromium engine automatically.

### <a id="DotNetBrowser_Engine_EngineOptions_ProprietaryFeatures"></a> ProprietaryFeatures

Gets the proprietary features enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public ProprietaryFeatures ProprietaryFeatures { get; }
```

#### Property Value

 [ProprietaryFeatures](DotNetBrowser.Engine.ProprietaryFeatures.md)

### <a id="DotNetBrowser_Engine_EngineOptions_RemoteDebuggingPort"></a> RemoteDebuggingPort

Gets the remote debugging port.

```csharp
public uint RemoteDebuggingPort { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### Remarks

<p>
    This option enables remote debugging over HTTP at the specific port. When remote
    debugging is enabled, you can navigate to the <code>http://localhost:&lt;port&gt;</code> address from
    another <code>Browser</code> instance or from the Google Chrome browser and debug the loaded web
    pages using Chrome DevTools. If you use Google Chrome browser for remote debugging, its
    version must be equal to the Chromium engine version that is used in DotNetBrowser.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_RenderingMode"></a> RenderingMode

Gets the rendering mode indicating how the content of the web pages will be rendered.

```csharp
public RenderingMode RenderingMode { get; }
```

#### Property Value

 [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

### <a id="DotNetBrowser_Engine_EngineOptions_Schemes"></a> Schemes

Gets the readonly dictionary of the schemes that will be intercepted.

```csharp
public IReadOnlyDictionary<Scheme, IHandler<InterceptRequestParameters, InterceptRequestResponse>> Schemes { get; }
```

#### Property Value

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[Scheme](DotNetBrowser.Net.Scheme.md), [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[InterceptRequestParameters](DotNetBrowser.Net.Handlers.InterceptRequestParameters.md), [InterceptRequestResponse](DotNetBrowser.Net.Handlers.InterceptRequestResponse.md)\>\>

### <a id="DotNetBrowser_Engine_EngineOptions_UserAgent"></a> UserAgent

Gets the custom user agent string that is used to override the default user agent for the
<xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
public string UserAgent { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Engine_EngineOptions_UserAgentMetadata"></a> UserAgentMetadata

Override profile client hints engine-wide.

```csharp
public UserAgentMetadata UserAgentMetadata { get; }
```

#### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

### <a id="DotNetBrowser_Engine_EngineOptions_UserDataDirectory"></a> UserDataDirectory

Gets an absolute path to the directory where the user data is stored.

```csharp
public string UserDataDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    The user data directory stores the data such as cache, cookies, history, GPU cache, local
    storage, visited links, web data, spell checking dictionary files, etc.
</p>
<p>
    <b>Important</b>: the user data directory cannot be used at the same time by multiple <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>
    instances running in a single or different applications.
</p>

## Methods

### <a id="DotNetBrowser_Engine_EngineOptions_IsProprietaryFeatureEnabled_DotNetBrowser_Engine_ProprietaryFeatures_"></a> IsProprietaryFeatureEnabled\(ProprietaryFeatures\)

Checks whether the given proprietary features are enabled.

```csharp
public bool IsProprietaryFeatureEnabled(ProprietaryFeatures proprietaryFeatures)
```

#### Parameters

`proprietaryFeatures` [ProprietaryFeatures](DotNetBrowser.Engine.ProprietaryFeatures.md)

the features to check.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the feature is enabled, false otherwise.

