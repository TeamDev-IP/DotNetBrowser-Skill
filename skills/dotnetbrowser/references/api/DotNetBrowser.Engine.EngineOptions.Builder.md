# <a id="DotNetBrowser_Engine_EngineOptions_Builder"></a> Class EngineOptions.Builder

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct engine options.

```csharp
public class EngineOptions.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineOptions.Builder](DotNetBrowser.Engine.EngineOptions.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

## Properties

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_AutoplayEnabled"></a> AutoplayEnabled

Enables or disables automatic video playback after page loading.

```csharp
public bool AutoplayEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_BinariesExtractionOptions"></a> BinariesExtractionOptions

Gets or sets the options that are used to configure the Chromium binaries extraction process.

```csharp
public BinariesExtractionOptions BinariesExtractionOptions { get; set; }
```

#### Property Value

 [BinariesExtractionOptions](DotNetBrowser.Engine.BinariesExtractionOptions.md)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ChromiumDirectory"></a> ChromiumDirectory

Gets or sets the absolute path to the directory where Chromium binaries are located or the empty
string if it was not set.

```csharp
public string ChromiumDirectory { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ChromiumSwitches"></a> ChromiumSwitches

Gets a set of the Chromium switches that will be passed to the Chromium Main
process.

```csharp
public HashSet<string> ChromiumSwitches { get; }
```

#### Property Value

 [HashSet](https://learn.microsoft.com/dotnet/api/system.collections.generic.hashset\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Remarks

<p>
    The library does not support all the possible Chromium switches, so there is no guarantee
    that the passed switches will work. The switches from this list will overwrite the
    corresponding options configured through the <xref href="DotNetBrowser.Engine.EngineOptions.Builder" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    For example, if you configure the remote debugging port using the<xref href="DotNetBrowser.Engine.EngineOptions.Builder.RemoteDebuggingPort" data-throw-if-not-resolved="false"></xref>
    property and then add the <code>--remote-debugging-port</code> switch using the
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.ChromiumSwitches" data-throw-if-not-resolved="false"></xref> property, then the port from the switch will
    be used.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_CrashDumpDirectory"></a> CrashDumpDirectory

Gets or sets the path that will be used to store automatically generated Chromium crash dumps.

```csharp
public string CrashDumpDirectory { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

If this property is set to null, the default path will be used. If this property is set to an empty string,
crash dump generation will be disabled.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_DiskCacheSize"></a> DiskCacheSize

Gets or sets the disk cache size.

```csharp
public long DiskCacheSize { get; set; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### Remarks

If the disk cache size was not set, then it will be calculated automatically. The size
depends on the available disk space in the volume where the disk cache is located.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_DnsOverHttpsDisabled"></a> DnsOverHttpsDisabled

Disables the DNS over HTTPS (DoH) protocol.

```csharp
public bool DnsOverHttpsDisabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    By default, DoH is enabled.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_FileAccessFromFilesAllowed"></a> FileAccessFromFilesAllowed

Allows or disallows the file access from files.

```csharp
public bool FileAccessFromFilesAllowed { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleApiKey"></a> GoogleApiKey

Gets or sets the Google API key.

```csharp
public string GoogleApiKey { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleDefaultClientId"></a> GoogleDefaultClientId

Gets or sets the Google client ID.

```csharp
public string GoogleDefaultClientId { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleDefaultClientSecret"></a> GoogleDefaultClientSecret

Gets or sets the Google client secret.

```csharp
public string GoogleDefaultClientSecret { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GpuDisabled"></a> GpuDisabled

Disables or enables GPU.

```csharp
public bool GpuDisabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_IncognitoEnabled"></a> IncognitoEnabled

Enables or disables the incognito mode for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public bool IncognitoEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

In the incognito mode the user data such as browsing history, cookies, site data, and the
information entered in forms are stored in memory and released once you close the <code>Engine</code>.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Language"></a> Language

Gets or sets the Chromium language that is used on the default error pages and message dialogs.

```csharp
public Language Language { get; set; }
```

#### Property Value

 [Language](DotNetBrowser.Ui.Language.md)

#### Remarks

<p>
    By default, the language is dynamically configured according to the default locale of the
    application. If the list of supported languages does not contain the language obtained from
    the application locale, then the US English language is used. This property allows you
    to override the default behavior and configure the Chromium engine with the given language.
</p>

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_LicenseKey"></a> LicenseKey

Gets or sets the license key.

```csharp
public string LicenseKey { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

The license key can be set via adding the "dotnetbrowser.license" file as embedded resource or individually
for every <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> using the <xref href="DotNetBrowser.Engine.EngineOptions.Builder.LicenseKey" data-throw-if-not-resolved="false"></xref> property.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_MediaRoutingEnabled"></a> MediaRoutingEnabled

Enables or disables the media routing.

<p>
    By default, it is disabled.
</p>

```csharp
public bool MediaRoutingEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_NativeKeyboardInputEnabled"></a> NativeKeyboardInputEnabled

Enables keyboard events processing using native system API in .NET.

<p>
    When not applied, the .NET keyboard listeners is used to collect key events, pre-handle them
    and dispatch to Chromium.
</p>
<p>
    When applied, the OS-specific API is used to collect key events from .NET with subsequent
    dispatch to Chromium.
</p>
<p>
    This option is not supported with <xref href="DotNetBrowser.Engine.RenderingMode.HardwareAccelerated" data-throw-if-not-resolved="false"></xref> on Windows
    and Linux. Engine creation throws <xref href="System.NotSupportedException" data-throw-if-not-resolved="false"></xref> for this
    combination.
</p>

```csharp
public bool NativeKeyboardInputEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_PasswordStore"></a> PasswordStore

Gets or sets the password store type which specifies the
storage backend should be used to encrypt cookies on Linux.

```csharp
public PasswordStore PasswordStore { get; set; }
```

#### Property Value

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

#### Remarks

If the password store type was not set, then the encryption storage backend is chosen by
Chromium engine automatically.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ProprietaryFeatures"></a> ProprietaryFeatures

Gets or sets the proprietary features enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.
By default, all the proprietary features are disabled.

```csharp
public ProprietaryFeatures ProprietaryFeatures { get; set; }
```

#### Property Value

 [ProprietaryFeatures](DotNetBrowser.Engine.ProprietaryFeatures.md)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_RemoteDebuggingPort"></a> RemoteDebuggingPort

Gets or sets the remote debugging port.

```csharp
public uint RemoteDebuggingPort { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_RenderingMode"></a> RenderingMode

Gets or sets the rendering mode indicating how the content of the web pages will be rendered.

```csharp
public RenderingMode RenderingMode { get; set; }
```

#### Property Value

 [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_SandboxDisabled"></a> SandboxDisabled

Enables or disables the sandbox.

```csharp
public bool SandboxDisabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Schemes"></a> Schemes

Gets the dictionary of the schemes that will be intercepted.

```csharp
public IDictionary<Scheme, IHandler<InterceptRequestParameters, InterceptRequestResponse>> Schemes { get; }
```

#### Property Value

 [IDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2)<[Scheme](DotNetBrowser.Net.Scheme.md), [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[InterceptRequestParameters](DotNetBrowser.Net.Handlers.InterceptRequestParameters.md), [InterceptRequestResponse](DotNetBrowser.Net.Handlers.InterceptRequestResponse.md)\>\>

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_TouchMenuDisabled"></a> TouchMenuDisabled

Enables or disables the touch popup menu.

```csharp
public bool TouchMenuDisabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserAgent"></a> UserAgent

Gets or sets the custom user agent string that is used to override the default user agent for the
<xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
public string UserAgent { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

This property has the same effect as adding the <code>--user-agent</code> switch.

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserAgentMetadata"></a> UserAgentMetadata

Override profile client hints engine-wide.

```csharp
public UserAgentMetadata UserAgentMetadata { get; set; }
```

#### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserDataDirectory"></a> UserDataDirectory

Gets or sets an absolute path to the directory where the user data is stored.

```csharp
public string UserDataDirectory { get; set; }
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

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_WebSecurityDisabled"></a> WebSecurityDisabled

Enables or disables the same-origin policy.

```csharp
public bool WebSecurityDisabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## Methods

### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public EngineOptions Build()
```

#### Returns

 [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

new <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

