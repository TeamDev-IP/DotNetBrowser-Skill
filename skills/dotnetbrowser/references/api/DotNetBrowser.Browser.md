# <a id="DotNetBrowser_Browser"></a> Namespace DotNetBrowser.Browser

### Namespaces

 [DotNetBrowser.Browser.Dialogs](DotNetBrowser.Browser.Dialogs.md)

 [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)

 [DotNetBrowser.Browser.FullScreen](DotNetBrowser.Browser.FullScreen.md)

 [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)

### Classes

 [BitmapTimeoutException](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BitmapTimeoutException)

Thrown when a bitmap request times out.

 [BrowserDisposeOptions](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserDisposeOptions)

The dispose options of the browser.

 [BrowserViewExtensions](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserViewExtensions)

Extension methods for <xref href="DotNetBrowser.Browser.IBrowserView" data-throw-if-not-resolved="false"></xref> interface.

 [UserAgentMetadata.Builder](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata_Builder)

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref>.

 [UserAgentBrandVersion.Builder](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion_Builder)

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref>.

 [CspParameters](DotNetBrowser.Browser.md#DotNetBrowser_Browser_CspParameters)

The parameters describing the particular key container within
a particular cryptographic service provider (CSP).

 [UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)

Contains the brand name and version type.

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

Contains the client hints data.

### Interfaces

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

A web browser control that allows loading a web page or a local HTML file, accessing DOM and
executing JavaScript on the loaded web page, getting notifications about loading progress,
dispatching keyboard and mouse events, etc.

 [IBrowserSettings](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowserSettings)

The settings of the browser.

 [IBrowserView](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowserView)

The interface that is implemented by UI components which are able to display the browser.

 [IDefaultFonts](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IDefaultFonts)

The default fonts used by a browser.

 [IOffScreenRenderProvider](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IOffScreenRenderProvider)

Provides access to an image rendered by the browser
that works in the off-screen rendering mode.

### Enums

 [PreferredColorScheme](DotNetBrowser.Browser.md#DotNetBrowser_Browser_PreferredColorScheme)

The preferred color scheme for the web content in the browser.

 [SavePageType](DotNetBrowser.Browser.md#DotNetBrowser_Browser_SavePageType)

Determines how the web page will be saved.

 [WebRtcIpHandlingPolicy](DotNetBrowser.Browser.md#DotNetBrowser_Browser_WebRtcIpHandlingPolicy)

The media performance/privacy tradeoffs which affect how WebRTC traffic will be routed and
how much local address information will be exposed.

## <a id="DotNetBrowser_Browser_BitmapTimeoutException"></a> Class BitmapTimeoutException

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Thrown when a bitmap request times out.

```csharp
public class BitmapTimeoutException : InvalidOperationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[SystemException](https://learn.microsoft.com/dotnet/api/system.systemexception) ← 
[InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception) ← 
[BitmapTimeoutException](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BitmapTimeoutException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[Exception.SerializeObjectState](https://learn.microsoft.com/dotnet/api/system.exception.serializeobjectstate), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Browser_BitmapTimeoutException__ctor"></a> BitmapTimeoutException\(\)

Constructs a new instance of <xref href="DotNetBrowser.Browser.BitmapTimeoutException" data-throw-if-not-resolved="false"></xref>.

```csharp
public BitmapTimeoutException()
```

## <a id="DotNetBrowser_Browser_BrowserDisposeOptions"></a> Class BrowserDisposeOptions

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The dispose options of the browser.

```csharp
public sealed class BrowserDisposeOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserDisposeOptions](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserDisposeOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_BrowserDisposeOptions_BeforeUnloadEventHandled"></a> BeforeUnloadEventHandled

Specifies whether the <code>beforeunload</code> and <code>unload</code> JavaScript events should be
handled if they are present on the web page loaded into the browser instance that is about to be disposed.

```csharp
public bool BeforeUnloadEventHandled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Browser_BrowserViewExtensions"></a> Class BrowserViewExtensions

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Browser.IBrowserView" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class BrowserViewExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserViewExtensions](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserViewExtensions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Browser_BrowserViewExtensions_InitializeFrom_DotNetBrowser_Browser_IBrowserView_DotNetBrowser_Browser_IBrowser_"></a> InitializeFrom\(IBrowserView, IBrowser\)

Initialize a browser view from this particular <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance. If there is another browser view
bound to this browser instance, that view will be de-initialized.

```csharp
public static void InitializeFrom(this IBrowserView browserView, IBrowser browser)
```

##### Parameters

`browserView` [IBrowserView](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowserView)

the browser view to initialize.

`browser` [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

the browser instance to initialize from.

## <a id="DotNetBrowser_Browser_CspParameters"></a> Class CspParameters

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The parameters describing the particular key container within
a particular cryptographic service provider (CSP).

```csharp
public sealed class CspParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CspParameters](DotNetBrowser.Browser.md#DotNetBrowser_Browser_CspParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_CspParameters_KeyContainerName"></a> KeyContainerName

Gets or sets the key container name.

```csharp
public string KeyContainerName { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_CspParameters_Pin"></a> Pin

Gets or sets the PIN associated with a smart card key.

```csharp
public string Pin { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

Use this property to supply a password for a smart card key.
When you specify a password using this property, a password dialog box
will not be presented to the user.

#### <a id="DotNetBrowser_Browser_CspParameters_ProviderName"></a> ProviderName

Gets or sets the cryptographic service provider (CSP) name.

```csharp
public string ProviderName { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_CspParameters_ProviderType"></a> ProviderType

Gets or sets the provider type.

```csharp
public int ProviderType { get; set; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Browser_UserAgentBrandVersion"></a> Class UserAgentBrandVersion

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Contains the brand name and version type.

```csharp
public class UserAgentBrandVersion
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Brand"></a> Brand

Gets the commercial name of the user agent or brand.

```csharp
public string Brand { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Version"></a> Version

Gets the version of the brand.

```csharp
public string Version { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder"></a> Class UserAgentBrandVersion.Builder

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UserAgentBrandVersion.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentBrandVersion.Builder](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

### Constructors

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder__ctor"></a> Builder\(\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentBrandVersion.Builder" data-throw-if-not-resolved="false"></xref>.

```csharp
public Builder()
```

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder__ctor_DotNetBrowser_Browser_UserAgentBrandVersion_"></a> Builder\(UserAgentBrandVersion\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentBrandVersion.Builder" data-throw-if-not-resolved="false"></xref> with an existing <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref>
instance.

```csharp
public Builder(UserAgentBrandVersion brandVersion)
```

##### Parameters

`brandVersion` [UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)

<xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance to initialize Builder.

### Properties

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Brand"></a> Brand

Gets or sets the commercial name of the user agent or brand.

```csharp
public string Brand { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Version"></a> Version

Gets or sets the version of the brand.

```csharp
public string Version { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public UserAgentBrandVersion Build()
```

##### Returns

 [UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)

new <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

## <a id="DotNetBrowser_Browser_UserAgentMetadata"></a> Class UserAgentMetadata

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Contains the client hints data.

```csharp
public class UserAgentMetadata
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Architecture"></a> Architecture

Gets the CPU architecture of the system.

```csharp
public string Architecture { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Bitness"></a> Bitness

Gets the bitness of the system architecture.

```csharp
public string Bitness { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_BrandFullVersionList"></a> BrandFullVersionList

Gets the list of brand and full versions. Typically, providing more detailed version information.

```csharp
public IReadOnlyList<UserAgentBrandVersion> BrandFullVersionList { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_BrandVersionList"></a> BrandVersionList

Gets the list of brand and major versions.

```csharp
public IReadOnlyList<UserAgentBrandVersion> BrandVersionList { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_FormFactors"></a> FormFactors

Gets the form-factors associated with the device.

```csharp
public IReadOnlyList<string> FormFactors { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_FullVersion"></a> FullVersion

Gets the full version string that corresponds to the user agent, or a brand in the brand list.

```csharp
public string FullVersion { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Mobile"></a> Mobile

Gets the mobile flag that show whether the client device is a mobile device.

```csharp
public bool Mobile { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Model"></a> Model

Gets the model name of the device running the user agent.

```csharp
public string Model { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Platform"></a> Platform

Gets the commercial name of the user agent's operating system.

```csharp
public string Platform { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_PlatformVersion"></a> PlatformVersion

Gets the version of the operating system running the user agent.

```csharp
public string PlatformVersion { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Wow64"></a> Wow64

Gets WOW64 flag that indicates if the user agent is running in 32-bit mode on a 64-bit Windows system.

```csharp
public bool Wow64 { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder"></a> Class UserAgentMetadata.Builder

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UserAgentMetadata.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentMetadata.Builder](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

### Constructors

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder__ctor"></a> Builder\(\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentMetadata.Builder" data-throw-if-not-resolved="false"></xref> is initialized with default values.

```csharp
public Builder()
```

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder__ctor_DotNetBrowser_Browser_UserAgentMetadata_"></a> Builder\(UserAgentMetadata\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentMetadata.Builder" data-throw-if-not-resolved="false"></xref> with an existing <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Builder(UserAgentMetadata metadata)
```

##### Parameters

`metadata` [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

<xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance to initialize Builder.

### Properties

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Architecture"></a> Architecture

Gets or sets the CPU architecture of the system.

```csharp
public string Architecture { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Bitness"></a> Bitness

Gets or sets bitness of the system architecture.

```csharp
public string Bitness { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_BrandFullVersionList"></a> BrandFullVersionList

Gets the list of brand and full versions. Typically, providing more detailed version information.

```csharp
public List<UserAgentBrandVersion> BrandFullVersionList { get; }
```

##### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_BrandVersionList"></a> BrandVersionList

Gets the list of brand and major versions.

```csharp
public List<UserAgentBrandVersion> BrandVersionList { get; }
```

##### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentBrandVersion)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_FormFactors"></a> FormFactors

Gets the form-factors associated with the device.

```csharp
public List<string> FormFactors { get; }
```

##### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_FullVersion"></a> FullVersion

Gets or sets the full version string that corresponds to the user agent, or a brand in the brand list.

```csharp
public string FullVersion { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Mobile"></a> Mobile

Gets or sets the mobile flag that show whether the client device is a mobile device.

```csharp
public bool Mobile { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Model"></a> Model

Gets or sets the model name of the device running the user agent.

```csharp
public string Model { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Platform"></a> Platform

Gets or sets the commercial name of the user agent's operating system.

```csharp
public string Platform { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_PlatformVersion"></a> PlatformVersion

Gets or sets the version of the operating system running the user agent.

```csharp
public string PlatformVersion { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Wow64"></a> Wow64

Gets or sets WOW64 flag that indicates if the user agent is running in 32-bit mode on a 64-bit Windows system.

```csharp
public bool Wow64 { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### Methods

#### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public UserAgentMetadata Build()
```

##### Returns

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

new <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

## <a id="DotNetBrowser_Browser_IBrowser"></a> Interface IBrowser

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A web browser control that allows loading a web page or a local HTML file, accessing DOM and
executing JavaScript on the loaded web page, getting notifications about loading progress,
dispatching keyboard and mouse events, etc.

```csharp
public interface IBrowser : IDisposable, IAutoDisposable
```

##### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

<p>
    The <code>IBrowser</code> instance itself is running in a separate native process that allocates
    memory and system resources that must be released. So, when a <code>IBrowser</code> instance is no
    longer needed, it must be disposed through the <xref href="System.IDisposable.Dispose" data-throw-if-not-resolved="false"></xref> method to release all the
    allocated memory and system resources. For example:
</p>

<pre><code class="lang-csharp">IBrowser browser = engine.CreateBrowser();
...
browser.Dispose();</code></pre>

<p>
    Any attempt to use an already disposed <code>IBrowser</code> instance will lead to the
    <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    The <code>IBrowser</code> instance is disposed automatically when its <code> IEngine</code> is disposed or
    unexpectedly crashed. If the instance represents a popup window created by JavaScript via the
    <code>window.open()</code> function, then JavaScript can close the instance using the
    <code>window.close()</code> function.
</p>
<p>
    To get notifications that the <code>IBrowser</code> instance has been disposed please subscribe to
    the following event:
</p>

<pre><code class="lang-csharp">browser.Disposed += (s, e) =&gt; {
    // The Browser instance has been disposed.
};</code></pre>

### Properties

#### <a id="DotNetBrowser_Browser_IBrowser_AllFrames"></a> AllFrames

Gets all the frames on the currently loaded web page.

```csharp
IEnumerable<IFrame> AllFrames { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance that allows controlling audio on the loaded web page and receive
notifications when audio has been
started or stopped playing.

```csharp
IAudio Audio { get; }
```

##### Property Value

 [IAudio](DotNetBrowser.Media.md#DotNetBrowser_Media_IAudio)

#### <a id="DotNetBrowser_Browser_IBrowser_Capture"></a> Capture

Gets the <xref href="DotNetBrowser.Capture.ICapture" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and handling capture sessions.

```csharp
ICapture Capture { get; }
```

##### Property Value

 [ICapture](DotNetBrowser.Capture.md#DotNetBrowser_Capture_ICapture)

#### <a id="DotNetBrowser_Browser_IBrowser_Cast"></a> Cast

Gets the <xref href="DotNetBrowser.Cast.ICast" data-throw-if-not-resolved="false"></xref> instance that can be used for casting media on receivers.

```csharp
ICast Cast { get; }
```

##### Property Value

 [ICast](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICast)

#### <a id="DotNetBrowser_Browser_IBrowser_ConvertJsNameHandler"></a> ConvertJsNameHandler

Gets or sets a handler that is used for the JavaScript name converting.
Implement this handler to have control of how the names are converted
when binding or executing JavaScript.

```csharp
IHandler<ConvertJsNameParameters, ConvertJsNameResponse> ConvertJsNameHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameParameters), [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)\>

##### Remarks

<p>
    The handler should be configured before registering .NET objects on the JavaScript side.
</p>
<p>
    The <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameParameters" data-throw-if-not-resolved="false"></xref> object contains information about the
    <xref href="System.Reflection.MemberInfo" data-throw-if-not-resolved="false"></xref> of the .NET object.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.NoConversion" data-throw-if-not-resolved="false"></xref> method to use the member name as is.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.CamelCase" data-throw-if-not-resolved="false"></xref> method to convert the first letter
    of the name to the lower case.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.PascalCase" data-throw-if-not-resolved="false"></xref> method to convert the first letter
    of the name to the upper case.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.ConvertTo(System.String)" data-throw-if-not-resolved="false"></xref> method for customizing the name.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_CreatePopupHandler"></a> CreatePopupHandler

Gets or sets a handler that is used when the browser decides whether a new popup instance can be created or not.

```csharp
IHandler<CreatePopupParameters, CreatePopupResponse> CreatePopupHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[CreatePopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupParameters), [CreatePopupResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupResponse)\>

##### Remarks

<p>Use the <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Create" data-throw-if-not-resolved="false"></xref> method to let the browser to create a new popup.</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Suppress" data-throw-if-not-resolved="false"></xref> method to suppress popup.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Suppress" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_CreditCards"></a> CreditCards

Gets the <xref href="DotNetBrowser.Card.ICreditCards" data-throw-if-not-resolved="false"></xref> instance that can be used for working with credit cards
saved in the Chromium credit card store.

```csharp
ICreditCards CreditCards { get; }
```

##### Property Value

 [ICreditCards](DotNetBrowser.Card.md#DotNetBrowser_Card_ICreditCards)

#### <a id="DotNetBrowser_Browser_IBrowser_DevTools"></a> DevTools

Gets the <xref href="DotNetBrowser.DevTools.IDevTools" data-throw-if-not-resolved="false"></xref> instance that allows working with Chromium Developer Tools for this browser.

```csharp
IDevTools DevTools { get; }
```

##### Property Value

 [IDevTools](DotNetBrowser.DevTools.md#DotNetBrowser_DevTools_IDevTools)

#### <a id="DotNetBrowser_Browser_IBrowser_Dialogs"></a> Dialogs

Gets the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs" data-throw-if-not-resolved="false"></xref> instance that can be used for configuring the dialogs that can be shown by
browser.

```csharp
IDialogs Dialogs { get; }
```

##### Property Value

 [IDialogs](DotNetBrowser.Browser.Dialogs.md#DotNetBrowser_Browser_Dialogs_IDialogs)

#### <a id="DotNetBrowser_Browser_IBrowser_DragAndDrop"></a> DragAndDrop

Gets the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> instance that can be used for managing drag&amp;drop operations for the
browser.

```csharp
IDragAndDrop DragAndDrop { get; }
```

##### Property Value

 [IDragAndDrop](DotNetBrowser.Input.DragAndDrop.md#DotNetBrowser_Input_DragAndDrop_IDragAndDrop)

#### <a id="DotNetBrowser_Browser_IBrowser_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Browser_IBrowser_Favicon"></a> Favicon

Gets the favicon of the currently loaded web page.

```csharp
Bitmap Favicon { get; }
```

##### Property Value

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

##### Remarks

Maximum favicon size is 16x16. If the actual favicon size is bigger, then it will be resized
to fit this constraint.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_FocusedFrame"></a> FocusedFrame

Gets the focused frame on the currently loaded web page.

```csharp
IFrame FocusedFrame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_FullScreen"></a> FullScreen

Gets the <xref href="DotNetBrowser.Browser.FullScreen.IFullScreen" data-throw-if-not-resolved="false"></xref> instance that can be used for controlling the browser's fullscreen mode.

```csharp
IFullScreen FullScreen { get; }
```

##### Property Value

 [IFullScreen](DotNetBrowser.Browser.FullScreen.md#DotNetBrowser_Browser_FullScreen_IFullScreen)

#### <a id="DotNetBrowser_Browser_IBrowser_InjectCssHandler"></a> InjectCssHandler

Gets or sets a handler that is used when the document element has been created and a custom stylesheet can
be injected into the document.

```csharp
IHandler<InjectCssParameters, InjectCssResponse> InjectCssHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[InjectCssParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssParameters), [InjectCssResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Inject(System.String)" data-throw-if-not-resolved="false"></xref> method to inject a custom stylesheet into the
    document.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Proceed" data-throw-if-not-resolved="false"></xref> method to continue loading without injecting.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Proceed" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_InjectJsHandler"></a> InjectJsHandler

Gets or sets a handler that is used when the document element has been created and a custom JavaScript can
be injected into the document.

```csharp
IHandler<InjectJsParameters> InjectJsHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[InjectJsParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectJsParameters)\>

##### Remarks

<p>
    You can inject a custom JavaScript code using the <xref href="DotNetBrowser.Frames.IFrame.ExecuteJavaScript(System.String%2cSystem.Boolean)" data-throw-if-not-resolved="false"></xref>
    method.This callback is intended to give you an opportunity to inject a .NET object into
    JavaScript code or inject a custom JavaScript code for further execution before any scripts are
    executed in the particular frame. For example:

<pre><code class="lang-csharp">Browser.InjectJsHandler = new Handler&lt;InjectJsParameters&gt;(args =&gt;
{
    IJsObject window = args.Frame.ExecuteJavaScript&lt;IJsObject&gt;("window").Result;
    window["myObject"] = new MyObject();
});</code></pre>

</p>
<p>
    The MyObject class may look like this:

<pre><code class="lang-csharp">public class MyObject
{
    public string SayHelloTo(string firstName) =&gt; "Hello " + firstName + "!";
}</code></pre>

</p>
<p>
    When the property is set, you can call methods of the injected .NET object from JavaScript:

<pre><code class="lang-csharp">window.myObject.SayHelloTo('John');</code></pre>

</p>
<p>This handler may be invoked several times for the same frame.</p>
<p>
    <b>Important:</b> you should avoid executing a JavaScript code that modifies the DOM tree of
    the web page being loaded.You must not use DotNetBrowser DOM API to remove the frame for which this
    callback is invoked, otherwise the render process will crash.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_JsDialogs"></a> JsDialogs

Gets the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs" data-throw-if-not-resolved="false"></xref> instance that can be used for configuring the JavaScript dialogs that can be
shown by browser.

```csharp
IJsDialogs JsDialogs { get; }
```

##### Property Value

 [IJsDialogs](DotNetBrowser.Browser.Dialogs.md#DotNetBrowser_Browser_Dialogs_IJsDialogs)

#### <a id="DotNetBrowser_Browser_IBrowser_Keyboard"></a> Keyboard

Gets the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and simulating keyboard input events.

```csharp
IKeyboard Keyboard { get; }
```

##### Property Value

 [IKeyboard](DotNetBrowser.Input.Keyboard.md#DotNetBrowser_Input_Keyboard_IKeyboard)

#### <a id="DotNetBrowser_Browser_IBrowser_MainFrame"></a> MainFrame

The main frame on the currently loaded web page, if it exists.

```csharp
IFrame MainFrame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_Mouse"></a> Mouse

Gets the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and simulating mouse input events.

```csharp
IMouse Mouse { get; }
```

##### Property Value

 [IMouse](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_IMouse)

#### <a id="DotNetBrowser_Browser_IBrowser_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance that can be used for controlling navigation in the current browser
instance.

```csharp
INavigation Navigation { get; }
```

##### Property Value

 [INavigation](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_INavigation)

#### <a id="DotNetBrowser_Browser_IBrowser_OpenExtensionActionPopupHandler"></a> OpenExtensionActionPopupHandler

Gets or sets a handler that is used for handling the popups that are requested to be shown by the extension action.

```csharp
IHandler<OpenExtensionActionPopupParameters> OpenExtensionActionPopupHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters)\>

##### Remarks

<p>
    The <xref href="DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters" data-throw-if-not-resolved="false"></xref> object contains the popup browser.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_OpenPopupHandler"></a> OpenPopupHandler

Gets or sets a handler that is used when a new popup browser instance should be opened.

```csharp
IHandler<OpenPopupParameters> OpenPopupHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[OpenPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenPopupParameters)\>

##### Remarks

<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_Passwords"></a> Passwords

Gets the <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> instance that can be used for working with logins and passwords
saved in the Chromium password store.

```csharp
IPasswords Passwords { get; }
```

##### Property Value

 [IPasswords](DotNetBrowser.Passwords.md#DotNetBrowser_Passwords_IPasswords)

#### <a id="DotNetBrowser_Browser_IBrowser_PrintHtmlContentHandler"></a> PrintHtmlContentHandler

Gets or sets a handler that is used when the HTML content printing is initiated.

```csharp
IHandler<PrintHtmlContentParameters, PrintHtmlContentResponse> PrintHtmlContentHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[PrintHtmlContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentParameters), [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)\>

##### Remarks

<p>
    In this callback you can configure the print settings. The workflow is the following:
</p>
<p>
    <ul><li>
            <returns>
                Find the required printer using the <xref href="DotNetBrowser.Print.IPrinters%602" data-throw-if-not-resolved="false"></xref>
                interface.
                You can obtain an instance of <code>Printers</code> using the
                <xref href="DotNetBrowser.Print.Handlers.PrintContentParameters%602.Printers" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>Get the current <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> from the printer.</returns>
        </li><li>
            <returns>
                Configure the required settings for the print job using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> interface provided by the
                <xref href="DotNetBrowser.Print.IPrintJob%601.Settings" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>
                Apply the configured settings using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method.
            </returns>
        </li><li>
            <returns>
                Tell the browser to proceed with the printing using the configured settings:
                <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IHtmlSettings%7d)" data-throw-if-not-resolved="false"></xref>.
            </returns>
        </li></ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IHtmlSettings%7d)" data-throw-if-not-resolved="false"></xref> method
    to continue printing using the selected printer.
</p>
<p>Use the <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    If printing is initiated when the browser is loading a web page, this callback is not
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_PrintPdfContentHandler"></a> PrintPdfContentHandler

Gets or sets a handler that is used when the PDF content printing is initiated.

```csharp
IHandler<PrintPdfContentParameters, PrintPdfContentResponse> PrintPdfContentHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[PrintPdfContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentParameters), [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)\>

##### Remarks

<p>
    In this callback you can configure the print settings. The workflow is the following:
</p>
<p>
    <ul><li>
            <returns>
                Find the required printer using the <xref href="DotNetBrowser.Print.IPrinters%602" data-throw-if-not-resolved="false"></xref>
                interface.
                You can obtain an instance of <code>Printers</code> using the
                <xref href="DotNetBrowser.Print.Handlers.PrintContentParameters%602.Printers" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>Get the current <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> from the printer.</returns>
        </li><li>
            <returns>
                Configure the required settings for the print job using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> interface provided by the
                <xref href="DotNetBrowser.Print.IPrintJob%601.Settings" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>
                Apply the configured settings using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method.
            </returns>
        </li><li>
            <returns>
                Tell the browser to proceed with the printing using the configured settings:
                <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IPdfSettings%7d)" data-throw-if-not-resolved="false"></xref>.
            </returns>
        </li></ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IPdfSettings%7d)" data-throw-if-not-resolved="false"></xref> method
    to continue printing using the selected printer.
</p>
<p>Use the <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    If printing is initiated when the browser is loading a web page, this callback is not
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

#### <a id="DotNetBrowser_Browser_IBrowser_RenderingMode"></a> RenderingMode

Gets the rendering mode of this browser.

```csharp
RenderingMode RenderingMode { get; }
```

##### Property Value

 [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

#### <a id="DotNetBrowser_Browser_IBrowser_RequestPdfDocumentPasswordHandler"></a> RequestPdfDocumentPasswordHandler

Gets or sets a handler that is used when the frame requests the password for an encrypted PDF document.

```csharp
IHandler<RequestPdfDocumentPasswordParameters, RequestPdfDocumentPasswordResponse> RequestPdfDocumentPasswordHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters), [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Password(System.String)" data-throw-if-not-resolved="false"></xref> method to
    provide the password for the encrypted PDF document.
</p>
<p>
    Use the<xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.ShowPasswordDialog" data-throw-if-not-resolved="false"></xref> method to
    invoke the default PDF viewer password dialog.
</p>
<p>
    Use the<xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to
    cancel the request.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_RequestPrintHandler"></a> RequestPrintHandler

Gets or sets a handler that is used when the printing is initiated.

```csharp
IHandler<RequestPrintParameters, RequestPrintResponse> RequestPrintHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[RequestPrintParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintParameters), [RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)\>

##### Remarks

<p>In this callback you can cancel or allow showing print preview dialog, or print the content programmatically.</p>
<p>By default, the printing is canceled if there is no browser view initialized from the browser.</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.ShowPrintPreview" data-throw-if-not-resolved="false"></xref> method to show the print preview.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Print" data-throw-if-not-resolved="false"></xref> method to continue printing and configure it programmatically
    in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    <b>Important:</b> do not use <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.ShowPrintPreview" data-throw-if-not-resolved="false"></xref> if the browser is not
    displayed. In this case, the dialog will not be visible  - as a result, the end user will not be able to
    close it or confirm printing.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_SelectCertificateHandler"></a> SelectCertificateHandler

Gets or sets a handler that is used when the web server requires authorization via client certificate.

```csharp
IHandler<SelectCertificateParameters, SelectCertificateResponse> SelectCertificateHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SelectCertificateParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateParameters), [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SelectCertificateResponse)\>

##### Remarks

<p>The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters" data-throw-if-not-resolved="false"></xref> object contains information about the authorization request.</p>
<p>
    To access the list of the certificates from the system storage that match the server criteria you
    can use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.Certificates" data-throw-if-not-resolved="false"></xref> property.
</p>
<p>
    You can use this handler to display a dialog with the list of the available certificates
    that allows the user to select the required certificate. Please note that it is not necessary to
    display a dialog in this handler.
</p>
<p>This handler itself is never called on the UI thread directly.</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the authorization.</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Select(System.Int32)" data-throw-if-not-resolved="false"></xref> method to inform the browser to use
    the client certificate located by the passed index in the certificate list.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Select(DotNetBrowser.Net.Certificates.Certificate)" data-throw-if-not-resolved="false"></xref> method to inform the
    browser to use the specified client certificate.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_Settings"></a> Settings

Gets the <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> instance that can be used for modifying the settings of the browser.

```csharp
IBrowserSettings Settings { get; }
```

##### Property Value

 [IBrowserSettings](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowserSettings)

#### <a id="DotNetBrowser_Browser_IBrowser_ShowContextMenuHandler"></a> ShowContextMenuHandler

Gets or sets a handler that is used when the browser should show a context menu.

```csharp
IHandler<ShowContextMenuParameters, ShowContextMenuResponse> ShowContextMenuHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuParameters), [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuResponse)\>

##### Remarks

<p>
    The passed <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuParameters" data-throw-if-not-resolved="false"></xref> object contains information about the context menu to show.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Close" data-throw-if-not-resolved="false"></xref> method to close the context menu without choice.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Select(DotNetBrowser.ContextMenu.ContextMenuItem)" data-throw-if-not-resolved="false"></xref> method to choose the context menu item.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Close" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_Size"></a> Size

Gets or sets the browser size.

```csharp
Size Size { get; set; }
```

##### Property Value

 [Size](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Size)

##### Remarks

<p>
    Setting this property updates the size of this Browser instance with the given width and height. Many web pages
    rely on the Browser's size and require that it's not empty. DOM document of a web page might not be loaded
    and displayed at all, because there's no sense in loading and rendering DOM document when it's empty.
</p>
<p>
    As a result, you should set the browser size programmatically when you don't need to display content of the
    loaded web page, but the web page must "think" it has been loaded in a browser instance
    with a non-empty size.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_StartDownloadHandler"></a> StartDownloadHandler

Gets or sets a handler that is used when the browser is about to start downloading the file.

```csharp
IHandler<StartDownloadParameters, StartDownloadResponse> StartDownloadHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[StartDownloadParameters](DotNetBrowser.Downloads.Handlers.md#DotNetBrowser_Downloads_Handlers_StartDownloadParameters), [StartDownloadResponse](DotNetBrowser.Downloads.Handlers.md#DotNetBrowser_Downloads_Handlers_StartDownloadResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.DownloadTo(System.String)" data-throw-if-not-resolved="false"></xref> method to
    confirm the download and specify the location to store the downloaded file.
</p>
<p>
    Use the<xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.Cancel" data-throw-if-not-resolved="false"></xref> method if you do not need
    to download the file.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownloads" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_TextFinder"></a> TextFinder

Gets the <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> instance that can be used for finding text on a web page loaded in the
browser.

```csharp
ITextFinder TextFinder { get; }
```

##### Property Value

 [ITextFinder](DotNetBrowser.Search.md#DotNetBrowser_Search_ITextFinder)

#### <a id="DotNetBrowser_Browser_IBrowser_Title"></a> Title

Gets the title of the currently loaded web page.

```csharp
string Title { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_Touch"></a> Touch

Gets the <xref href="DotNetBrowser.Input.Touch.ITouch" data-throw-if-not-resolved="false"></xref> instance that can be used for listening touch input events.

```csharp
ITouch Touch { get; }
```

##### Property Value

 [ITouch](DotNetBrowser.Input.Touch.md#DotNetBrowser_Input_Touch_ITouch)

#### <a id="DotNetBrowser_Browser_IBrowser_Url"></a> Url

Gets the URL of the currently loaded web page or an empty string if
the browser hasn't loaded any web page yet.

```csharp
string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_UserAgent"></a> UserAgent

Gets or sets the <code>user-agent</code> of the current browser instance.

```csharp
string UserAgent { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_UserAgentMetadata"></a> UserAgentMetadata

Gets or sets the <code>user-agent metadata</code>, known as client hints, of the current browser instance.

```csharp
UserAgentMetadata UserAgentMetadata { get; set; }
```

##### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_UserDataProfiles"></a> UserDataProfiles

Gets the <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> instance that can be used for working with user data profiles
saved in the Chromium user data store.

```csharp
IUserDataProfiles UserDataProfiles { get; }
```

##### Property Value

 [IUserDataProfiles](DotNetBrowser.UserData.md#DotNetBrowser_UserData_IUserDataProfiles)

#### <a id="DotNetBrowser_Browser_IBrowser_Zoom"></a> Zoom

Gets the <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance that can be used for zooming content of a web page loaded in the current
browser instance.

```csharp
IZoom Zoom { get; }
```

##### Property Value

 [IZoom](DotNetBrowser.Zoom.md#DotNetBrowser_Zoom_IZoom)

### Methods

#### <a id="DotNetBrowser_Browser_IBrowser_DisposeAsync_DotNetBrowser_Browser_BrowserDisposeOptions_"></a> DisposeAsync\(BrowserDisposeOptions\)

Asynchronously disposes the current browser instance according to the given options.

```csharp
Task<bool> DisposeAsync(BrowserDisposeOptions browserDisposeOptions)
```

##### Parameters

`browserDisposeOptions` [BrowserDisposeOptions](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserDisposeOptions)

browser dispose options.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

The task that represents the result of the asynchronous dispose process.
<code>True</code> indicates that the browser instance is successfully disposed without any dialogs,
<code>false</code> if the dispose process was canceled.
This may happen if the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> handler was invoked and
the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.Stay" data-throw-if-not-resolved="false"></xref> response was sent.

##### Remarks

<p>
    If the currently loaded web page registers the <code>onbeforeunload</code> JavaScript event
    and the given options tell the browser to fire the <code>beforeunload</code>
    event, then this method will not dispose the browser right away.
</p>
<p>
    The <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> will be invoked
    in this case and if the handler tells the browser to stay on the web page, then the browser
    will not be disposed.
</p>
<p>
    The following example demonstrates how to dispose the browser instance as if a user
    manually clicking the close button of the tab/window.
</p>

<pre><code class="lang-csharp">browser.DisposeAsync(new BrowserDisposeOptions(){BeforeUnloadEventHandled = true});</code></pre>

<p>
    If the browser is already disposed, then this method does nothing.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_DownloadResource_System_String_"></a> DownloadResource\(string\)

Starts downloading the resource at the specified URL.

```csharp
void DownloadResource(string url)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to download.

##### Remarks

If the given URL is valid and points to a downloadable resource, then the
download process will be started. To control the download process, use
<xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>.

<p>
    The method does nothing if the given URL is not well-formed or points to a resource
    that cannot be downloaded.
</p>

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty, or consists only of white-space
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_Focus"></a> Focus\(\)

Tells the browser that it has focus and must be activated.

```csharp
void Focus()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_ReplaceMisspelledWord_System_String_"></a> ReplaceMisspelledWord\(string\)

Replaces misspelled word under cursor on the currently loaded web page with the given <code class="paramref">word</code>.
If there is no misspelled word under cursor, this method does nothing.

```csharp
void ReplaceMisspelledWord(string word)
```

##### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the word for replacement

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code> is null, empty, or consists only of white-space
characters.

#### <a id="DotNetBrowser_Browser_IBrowser_SaveWebPage_System_String_System_String_DotNetBrowser_Browser_SavePageType_"></a> SaveWebPage\(string, string, SavePageType\)

Initiates the saving process of the currently loaded web page. The web page can be saved as a
single HTML file or the file with resources. Before saving a web page make sure that it is
not being loaded. It is recommended to completely loaded the web page and only then save it.

```csharp
bool SaveWebPage(string filePath, string resourcesPath, SavePageType saveType)
```

##### Parameters

`filePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

an absolute path to a file in which the web page will be saved.

`resourcesPath` [string](https://learn.microsoft.com/dotnet/api/system.string)

an absolute path to a directory in which the resources (e.g. images, css)
of the web page will be saved. If the directory does not exist, it will
be created

`saveType` [SavePageType](DotNetBrowser.Browser.md#DotNetBrowser_Browser_SavePageType)

determines how the web page will be saved: as an HTML file with all the
required resources (e.g. images, css etc.), a single HTML or MHTML file

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the saving process has been initialized successfully, <code>false</code> otherwise.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">filePath</code> is null, empty, or consists only of white-space
characters.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">resourcesPath</code> is null, empty, or consists only of
white-space characters.

#### <a id="DotNetBrowser_Browser_IBrowser_SetPrivateKeyProviderPin_DotNetBrowser_Browser_CspParameters_"></a> SetPrivateKeyProviderPin\(CspParameters\)

Sets the key exchange PIN for the particular cryptographic
service provider (CSP) and the particular key container in it.
This functionality can be used to set the PIN that is requested when
trying to use a client certificate stored on the smart card.

```csharp
bool SetPrivateKeyProviderPin(CspParameters cspParameters)
```

##### Parameters

`cspParameters` [CspParameters](DotNetBrowser.Browser.md#DotNetBrowser_Browser_CspParameters)

The parameters of the private key CSP container.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the PIN was set successfully, <code>false</code> otherwise.

##### Remarks

<p>
    This functionality is Windows-only. The implementation will
    return false in other environments.
</p>
<p>If the PIN was not set successfully, the actual error will be written to DotNetBrowser logs.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cspParameters</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Any of the required parameters in <code class="paramref">cspParameters</code> is null, empty, or consists only of
white-space characters.

#### <a id="DotNetBrowser_Browser_IBrowser_TakeImage"></a> TakeImage\(\)

Creates and returns an image of the currently loaded web page.

```csharp
Bitmap TakeImage()
```

##### Returns

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

a <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> that contains the image of the currently loaded web page.

##### Remarks

<p>
    The bitmap size depends on the size of the current browser instance and the device scale
    factor of the display where it is located at the moment. If the current browser size is
    empty, then the bitmap will be empty as well.
</p>
<p>
    For example, if the device scale factor of the display where the browser instance is
    located at the moment is 2.0 and the browser size is 100x100, then the size of the bitmap is
    expected to be 200x200.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

 [BitmapTimeoutException](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BitmapTimeoutException)

The <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> can not be retrieved within <code>10</code> seconds.

#### <a id="DotNetBrowser_Browser_IBrowser_Unfocus"></a> Unfocus\(\)

Tells the browser that it does not have focus and must be deactivated.

```csharp
void Unfocus()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowser_BrowserBecameResponsive"></a> BrowserBecameResponsive

Occurs when the browser instance has become responsive.

```csharp
event EventHandler<BrowserBecameResponsiveEventArgs> BrowserBecameResponsive
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[BrowserBecameResponsiveEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserBecameResponsiveEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_BrowserBecameUnresponsive"></a> BrowserBecameUnresponsive

Occurs when the browser instance has become unresponsive.

```csharp
event EventHandler<BrowserBecameUnresponsiveEventArgs> BrowserBecameUnresponsive
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[BrowserBecameUnresponsiveEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserBecameUnresponsiveEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_ConsoleMessageReceived"></a> ConsoleMessageReceived

Occurs when the message was added to the console.

```csharp
event EventHandler<ConsoleMessageReceivedEventArgs> ConsoleMessageReceived
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ConsoleMessageReceivedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_ConsoleMessageReceivedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FaviconChanged"></a> FaviconChanged

Occurs when the web page favicon has changed.

```csharp
event EventHandler<FaviconChangedEventArgs> FaviconChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FaviconChangedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FaviconChangedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FocusGained"></a> FocusGained

Occurs when the browser instance has gained the focus.

```csharp
event EventHandler<FocusGainedEventArgs> FocusGained
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusGainedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FocusGainedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FocusLost"></a> FocusLost

Occurs when the browser instance has lost the focus.

```csharp
event EventHandler<FocusLostEventArgs> FocusLost
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusLostEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FocusLostEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FocusRequested"></a> FocusRequested

Occurs when JavaScript sends a request to focus the Browser instance by calling the
<code>window.focus()</code> method.

```csharp
event EventHandler<FocusRequestedEventArgs> FocusRequested
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusRequestedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FocusRequestedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FrameCreated"></a> FrameCreated

Occurs when the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been created.

```csharp
event EventHandler<FrameCreatedEventArgs> FrameCreated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameCreatedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FrameCreatedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_FrameDeleted"></a> FrameDeleted

Occurs when the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been deleted.

```csharp
event EventHandler<FrameDeletedEventArgs> FrameDeleted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameDeletedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_FrameDeletedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_MediaStreamCaptureStarted"></a> MediaStreamCaptureStarted

Occurs when the web page has started capturing an audio or video stream.

```csharp
event EventHandler<MediaStreamCaptureStartedEventArgs> MediaStreamCaptureStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaStreamCaptureStartedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_MediaStreamCaptureStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_MediaStreamCaptureStopped"></a> MediaStreamCaptureStopped

Occurs when the web page has stopped capturing an audio or video stream.

```csharp
event EventHandler<MediaStreamCaptureStoppedEventArgs> MediaStreamCaptureStopped
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaStreamCaptureStoppedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_MediaStreamCaptureStoppedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_PdfDocumentLoadFailed"></a> PdfDocumentLoadFailed

Occurs when a PDF document failed to load in a frame.

```csharp
event EventHandler<PdfDocumentLoadFailedEventArgs> PdfDocumentLoadFailed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PdfDocumentLoadFailedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_PdfDocumentLoadFailedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_PdfDocumentLoaded"></a> PdfDocumentLoaded

Occurs when a PDF document has been successfully loaded in a frame.

```csharp
event EventHandler<PdfDocumentLoadedEventArgs> PdfDocumentLoaded
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PdfDocumentLoadedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_PdfDocumentLoadedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_PrintPreviewClosed"></a> PrintPreviewClosed

Occurs when print preview dialog is closed.

```csharp
event EventHandler<PrintPreviewClosedEventArgs> PrintPreviewClosed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintPreviewClosedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_PrintPreviewClosedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_PrintPreviewOpened"></a> PrintPreviewOpened

Occurs when print preview dialog is opened.

```csharp
event EventHandler<PrintPreviewOpenedEventArgs> PrintPreviewOpened
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintPreviewOpenedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_PrintPreviewOpenedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_RenderProcessTerminated"></a> RenderProcessTerminated

Occurs when a render process has been terminated.

```csharp
event EventHandler<RenderProcessTerminatedEventArgs> RenderProcessTerminated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RenderProcessTerminatedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_RenderProcessTerminatedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_SpellCheckCompleted"></a> SpellCheckCompleted

Occurs when spell checking on the frame has been completed.

```csharp
event EventHandler<SpellCheckCompletedEventArgs> SpellCheckCompleted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SpellCheckCompletedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_SpellCheckCompletedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_StatusChanged"></a> StatusChanged

Occurs when the status text has been changed.

```csharp
event EventHandler<StatusChangedEventArgs> StatusChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[StatusChangedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_StatusChangedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_TitleChanged"></a> TitleChanged

Occurs when the web page title has been changed.

```csharp
event EventHandler<TitleChangedEventArgs> TitleChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[TitleChangedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_TitleChangedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IBrowser_UpdateBoundsRequested"></a> UpdateBoundsRequested

Occurs when JavaScript requests to update bounds of the Browser instance.

```csharp
event EventHandler<UpdateBoundsRequestedEventArgs> UpdateBoundsRequested
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[UpdateBoundsRequestedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_UpdateBoundsRequestedEventArgs)\>

##### Remarks

JavaScript can request to update bounds of the Browser instance through the
following JavaScript functions:

<ul><li><span class="term">
            <code>window.moveTo()</code>
        </span>
            moves a window to the specified position.
        </li><li><span class="term">
            <code>window.moveBy()</code>
        </span>
            moves a window a specified number of pixels relative to its
            current coordinates.
        </li><li><span class="term">
            <code>window.resizeTo()</code>
        </span>
            resizes the window to the specified width and height.
        </li><li><span class="term">
            <code>window.resizeBy()</code>
        </span>
            resizes the window by the specified pixels.
        </li></ul>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Browser_IBrowserSettings"></a> Interface IBrowserSettings

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The settings of the browser.

```csharp
public interface IBrowserSettings : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowJavaScriptAccessClipboard"></a> AllowJavaScriptAccessClipboard

Allows or disallows JavaScript code on the web pages loaded in the browser to access clipboard.

```csharp
bool AllowJavaScriptAccessClipboard { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowLoadingImagesAutomatically"></a> AllowLoadingImagesAutomatically

Allows or disallows loading images automatically on the web pages loaded in the browser.

```csharp
bool AllowLoadingImagesAutomatically { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowRunningInsecureContent"></a> AllowRunningInsecureContent

Allows or disallows running an insecure content in the browser.

```csharp
bool AllowRunningInsecureContent { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_AllowScriptsToCloseWindows"></a> AllowScriptsToCloseWindows

Allows or disallows JavaScript code on the web pages loaded in the browser to close the browser.

```csharp
bool AllowScriptsToCloseWindows { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultBackgroundColor"></a> DefaultBackgroundColor

Gets or sets the default browser background color.

```csharp
Color DefaultBackgroundColor { get; set; }
```

##### Property Value

 [Color](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Color)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultEncoding"></a> DefaultEncoding

Gets or sets the default text encoding.

```csharp
string DefaultEncoding { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultFontSize"></a> DefaultFontSize

Gets or sets the default browser font size.

```csharp
FontSize DefaultFontSize { get; set; }
```

##### Property Value

 [FontSize](DotNetBrowser.Ui.md#DotNetBrowser_Ui_FontSize)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_DefaultFonts"></a> DefaultFonts

Gets the default fonts used by the browser.

```csharp
IDefaultFonts DefaultFonts { get; }
```

##### Property Value

 [IDefaultFonts](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IDefaultFonts)

##### Remarks

The returned object belongs to this browser and can be used while the browser is alive.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_ImagesEnabled"></a> ImagesEnabled

Enables or disables images displaying on the web pages loaded in the browser.

```csharp
bool ImagesEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_JavaScriptEnabled"></a> JavaScriptEnabled

Enables or disables JavaScript on the web pages loaded in the browser.

```csharp
bool JavaScriptEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_LocalStorageEnabled"></a> LocalStorageEnabled

Enables or disables the local storage in the browser.

```csharp
bool LocalStorageEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_OverscrollHistoryNavigationEnabled"></a> OverscrollHistoryNavigationEnabled

Enables or disables the back/forward navigation with a left/right swipe in the browser.

```csharp
bool OverscrollHistoryNavigationEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_PluginsEnabled"></a> PluginsEnabled

Enables or disables plugins on the web pages loaded in the browser.

```csharp
bool PluginsEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_PreferredColorScheme"></a> PreferredColorScheme

Gets or sets the preferred color scheme for the web content in the browser.

```csharp
PreferredColorScheme PreferredColorScheme { get; set; }
```

##### Property Value

 [PreferredColorScheme](DotNetBrowser.Browser.md#DotNetBrowser_Browser_PreferredColorScheme)

##### Remarks

The scheme is used to evaluate the <code>prefers-color-scheme</code> media query and resolve UA color scheme to be used
based on the <code>supported-color-schemes</code> META tag and CSS property.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_ScrollbarsHidden"></a> ScrollbarsHidden

Hides or shows scrollbars on the web pages.

```csharp
bool ScrollbarsHidden { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_TransparentBackgroundEnabled"></a> TransparentBackgroundEnabled

Enables or disables transparent background on the web pages.By default, the background is always
opaque.

```csharp
bool TransparentBackgroundEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

<p>
    This property supports only the <xref href="DotNetBrowser.Engine.RenderingMode.OffScreen" data-throw-if-not-resolved="false"></xref> rendering mode
    on Windows and Linux, and the both rendering modes on macOS.
</p>
<p>
    The attempt to set this property to <code>true</code> in the unsupported rendering mode will result in an
    exception.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IBrowserSettings_WebRtcIpHandlingPolicy"></a> WebRtcIpHandlingPolicy

Gets or sets the WebRTC IP handling policy for the browser.

```csharp
WebRtcIpHandlingPolicy WebRtcIpHandlingPolicy { get; set; }
```

##### Property Value

 [WebRtcIpHandlingPolicy](DotNetBrowser.Browser.md#DotNetBrowser_Browser_WebRtcIpHandlingPolicy)

##### Remarks

Specifying the custom WebRTC IP handling policy can be used to protect against WebRTC leaks - the WebRTC itself
will remain enabled.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Browser_IBrowserView"></a> Interface IBrowserView

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The interface that is implemented by UI components which are able to display the browser.

```csharp
public interface IBrowserView
```

##### Extension Methods

[BrowserViewExtensions.InitializeFrom\(IBrowserView, IBrowser\)](DotNetBrowser.Browser.md#DotNetBrowser_Browser_BrowserViewExtensions_InitializeFrom_DotNetBrowser_Browser_IBrowserView_DotNetBrowser_Browser_IBrowser_)

## <a id="DotNetBrowser_Browser_IDefaultFonts"></a> Interface IDefaultFonts

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The default fonts used by a browser.

```csharp
public interface IDefaultFonts
```

### Remarks

An instance of this interface belongs to a browser and can be used while the browser is alive.

### Properties

#### <a id="DotNetBrowser_Browser_IDefaultFonts_Available"></a> Available

Gets the system fonts available to the browser.

```csharp
IReadOnlyList<Font> Available { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)\>

##### Remarks

The available fonts depend on the operating system and the fonts installed on it.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IDefaultFonts_FixedWidth"></a> FixedWidth

Gets or sets the fixed-width font used by the browser.

```csharp
Font FixedWidth { get; set; }
```

##### Property Value

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IDefaultFonts_Mathematical"></a> Mathematical

Gets or sets the mathematical font used by the browser.

```csharp
Font Mathematical { get; set; }
```

##### Property Value

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IDefaultFonts_SansSerif"></a> SansSerif

Gets or sets the sans-serif font used by the browser.

```csharp
Font SansSerif { get; set; }
```

##### Property Value

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IDefaultFonts_Serif"></a> Serif

Gets or sets the serif font used by the browser.

```csharp
Font Serif { get; set; }
```

##### Property Value

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_IDefaultFonts_Standard"></a> Standard

Gets or sets the standard font used by the browser.

```csharp
Font Standard { get; set; }
```

##### Property Value

 [Font](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Font)

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Browser_IOffScreenRenderProvider"></a> Interface IOffScreenRenderProvider

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Provides access to an image rendered by the browser
that works in the off-screen rendering mode.

```csharp
public interface IOffScreenRenderProvider
```

### Properties

#### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_PaintHandler"></a> PaintHandler

Gets or sets a handler that is used when the browser contents should be rendered.

```csharp
IHandler<PaintParameters> PaintHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<PaintParameters\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_Hide"></a> Hide\(\)

Tells the browser to stop rendering its content as if it was hidden.

```csharp
void Hide()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_Show"></a> Show\(\)

Tells the browser to start rendering its content as if it was shown on the screen.

```csharp
void Show()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_CursorChanged"></a> CursorChanged

Occurs when the cursor should be changed.

```csharp
event EventHandler<CursorChangedEventArgs> CursorChanged
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CursorChangedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_CursorChangedEventArgs)\>

## <a id="DotNetBrowser_Browser_PreferredColorScheme"></a> Enum PreferredColorScheme

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The preferred color scheme for the web content in the browser.

```csharp
public enum PreferredColorScheme
```

### Fields

`Dark = 1` 

The dark color scheme is preferred.



`Light = 2` 

The light color scheme is preferred.



### Remarks

The scheme is used to evaluate the <code>prefers-color-scheme</code> media query and resolve UA color scheme to be used
based on the <code>supported-color-schemes</code> META tag and CSS property.

## <a id="DotNetBrowser_Browser_SavePageType"></a> Enum SavePageType

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Determines how the web page will be saved.

```csharp
public enum SavePageType
```

### Fields

`CompletePage = 2` 

HTML file with required resources (e.g. images, css etc.).



`Html = 1` 

Single HTML.



`MHtml = 3` 

MHTML file.

## <a id="DotNetBrowser_Browser_WebRtcIpHandlingPolicy"></a> Enum WebRtcIpHandlingPolicy

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The media performance/privacy tradeoffs which affect how WebRTC traffic will be routed and
how much local address information will be exposed.

```csharp
public enum WebRtcIpHandlingPolicy
```

### Fields

`Default = 1` 

This is the default behavior. Currently, WebRTC has the right to enumerate
all interfaces and bind them to discover public interfaces.



`DefaultPublicAndPrivateInterfaces = 3` 

WebRTC should only use the default route used by HTTP. This also exposes the
associated default private address. Default route is the route chosen by the
OS on a multi-homed endpoint.



`DefaultPublicInterfacesOnly = 2` 

WebRTC should only use the default route used by HTTP. This doesn't expose
any local addresses.



`DisableNonProxiedUdp = 4` 

WebRTC should only use TCP to contact peers or servers unless the proxy
server supports UDP. This doesn't expose any local addresses either.
