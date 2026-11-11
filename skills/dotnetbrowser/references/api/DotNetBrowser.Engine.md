# <a id="DotNetBrowser_Engine"></a> Namespace DotNetBrowser.Engine

### Namespaces

 [DotNetBrowser.Engine.Events](DotNetBrowser.Engine.Events.md)

### Classes

 [AutoDeElevationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_AutoDeElevationException)

Thrown when Chromium is launched with admin permissions on Windows and restarts itself
without them, which DotNetBrowser does not support.

 [BinariesExtractionOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesExtractionOptions)

The options that are used to configure the Chromium binaries extraction process.

 [EngineOptions.Builder](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions_Builder)

A builder class to construct engine options.

 [ChromiumBinariesMissingException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ChromiumBinariesMissingException)

Thrown when the engine initialization fails due to missing compatible Chromium binaries.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The exception thrown when the connection to the Chromium engine appears to be closed.

 [EngineFactory](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineFactory)

Factory class that is used to create <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

 [EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException)

The base class for those exceptions that can be thrown during <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization.

 [EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

The options that are used to configure <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

 [InvalidLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_InvalidLicenseException)

Thrown when the given license is invalid.

 [LicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_LicenseException)

The base class for those exceptions that can be thrown during license checking.

 [MissingDependencyException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_MissingDependencyException)

Thrown when Chromium fails to find the required system libraries on Linux.

 [NoLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_NoLicenseException)

Thrown when no license found.

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

Defines password store types that are used to specify which encryption storage backend to use to
encrypt cookies on Linux.

 [SandboxNotSupportedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_SandboxNotSupportedException)

Thrown when the current environment does not support creating processes within a new user namespace,
preventing Chromium from being launched in sandbox mode.

 [UserDataCreationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataCreationException)

Thrown when the user data directory cannot be created.

 [UserDataInUseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataInUseException)

Thrown when the user data directory is already in use by another Chromium engine instance.

### Interfaces

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

Provides access to the Chromium engine functionality.

 [IWidevine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IWidevine)

The Widevine DRM (Digital Rights Management) component.

### Enums

 [BinariesVerificationLevel](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesVerificationLevel)

The level of the Chromium binaries verification.

 [ProprietaryFeatures](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ProprietaryFeatures)

The list of supported proprietary features.

 [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

The supported rendering modes.

 [Theme](DotNetBrowser.Engine.md#DotNetBrowser_Engine_Theme)

The Chromium theme, which affects the appearanceof web pages and their contents,
as well as Chromium dialogs, such as Print Preview and DevTools.

 [WidevineActivationStatus](DotNetBrowser.Engine.md#DotNetBrowser_Engine_WidevineActivationStatus)

Represents the result of attempting to activate the Widevine component.

## <a id="DotNetBrowser_Engine_AutoDeElevationException"></a> Class AutoDeElevationException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when Chromium is launched with admin permissions on Windows and restarts itself
without them, which DotNetBrowser does not support.

```csharp
public sealed class AutoDeElevationException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[AutoDeElevationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_AutoDeElevationException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    When this exception is thrown, run the application without admin permissions, or keep them by adding
    the <code>--do-not-de-elevate</code> switch to <xref href="DotNetBrowser.Engine.EngineOptions.Builder.ChromiumSwitches" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    For more information, see
    <a href="https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/common-issues/#running-as-admin-on-windows">https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/common-issues/#running-as-admin-on-windows</a>.
</p>

## <a id="DotNetBrowser_Engine_BinariesExtractionOptions"></a> Class BinariesExtractionOptions

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The options that are used to configure the Chromium binaries extraction process.

```csharp
public sealed class BinariesExtractionOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BinariesExtractionOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesExtractionOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Engine_BinariesExtractionOptions__ctor_System_String_"></a> BinariesExtractionOptions\(string\)

Creates and initializes an instance of <xref href="DotNetBrowser.Engine.BinariesExtractionOptions" data-throw-if-not-resolved="false"></xref>.

```csharp
public BinariesExtractionOptions(string additionalBinariesSearchPath = null)
```

##### Parameters

`additionalBinariesSearchPath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The additional custom path to search for an assembly containing compatible
Chromium binaries.

### Properties

#### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_AdditionalBinariesSearchPath"></a> AdditionalBinariesSearchPath

Gets the additional custom path to search for an assembly containing compatible Chromium binaries.

```csharp
public string AdditionalBinariesSearchPath { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_CheckLinuxDependencies"></a> CheckLinuxDependencies

Indicates whether it is necessary to check if Linux environment has all required shared libraries.

```csharp
public bool CheckLinuxDependencies { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

<p>
    By default, the check is performed.
</p>
<p>
    If <code>false</code>, this step is skipped. It's useful for clients that are confident in their
    environments.
</p>
<p>
    The <code>ldd</code> command is used to check presence of the libraries required
    by Chromium executable.
</p>

#### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_Chromium64BitPreferred"></a> Chromium64BitPreferred

Indicates whether 64-bit Chromium binaries are preferred when possible.

```csharp
public bool Chromium64BitPreferred { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

<p>By default, the bitness of the Chromium process will match the bitness of the .NET process.</p>
<p>
    However, when this option is set to true, the .NET process is 32-bit, and the operating system is 64-bit,
    DotNetBrowser will try using the 64-bit Chromium binaries.
</p>

#### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_VerificationLevel"></a> VerificationLevel

Gets or sets the binaries verification level.

```csharp
public BinariesVerificationLevel VerificationLevel { get; set; }
```

##### Property Value

 [BinariesVerificationLevel](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesVerificationLevel)

##### Remarks

By default, the binaries verification level is set to <xref href="DotNetBrowser.Engine.BinariesVerificationLevel.Normal" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Engine_ChromiumBinariesMissingException"></a> Class ChromiumBinariesMissingException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the engine initialization fails due to missing compatible Chromium binaries.

```csharp
public class ChromiumBinariesMissingException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[ChromiumBinariesMissingException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ChromiumBinariesMissingException)

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

#### <a id="DotNetBrowser_Engine_ChromiumBinariesMissingException__ctor_System_String_"></a> ChromiumBinariesMissingException\(string\)

Initializes a new instance with the specified <code class="paramref">message</code>.

```csharp
public ChromiumBinariesMissingException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

The detailed message.

## <a id="DotNetBrowser_Engine_ConnectionClosedException"></a> Class ConnectionClosedException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The exception thrown when the connection to the Chromium engine appears to be closed.

```csharp
public class ConnectionClosedException : InvalidOperationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[SystemException](https://learn.microsoft.com/dotnet/api/system.systemexception) ← 
[InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception) ← 
[ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

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

## <a id="DotNetBrowser_Engine_EngineFactory"></a> Class EngineFactory

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.Core.dll  

Factory class that is used to create <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

```csharp
public static class EngineFactory
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineFactory](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineFactory)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Engine_EngineFactory_Create_DotNetBrowser_Engine_EngineOptions_"></a> Create\(EngineOptions\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create(EngineOptions options)
```

##### Parameters

`options` [EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

The <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance that will be used for initializing the engine

##### Returns

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

A completely initialized Chromium engine.

##### Examples

<pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = EngineFactory.Create(engineOptions);</code></pre>

##### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

Native keyboard input is enabled with hardware-accelerated rendering on Windows or Linux.

#### <a id="DotNetBrowser_Engine_EngineFactory_Create_DotNetBrowser_Engine_RenderingMode_"></a> Create\(RenderingMode\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create(RenderingMode renderingMode)
```

##### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

The <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> that will be used for initializing the engine.

##### Returns

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

A completely initialized Chromium engine.

##### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.Create(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling
<code>new EngineOptions.Builder().Build()</code> with the <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> specified.

##### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

#### <a id="DotNetBrowser_Engine_EngineFactory_Create"></a> Create\(\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create()
```

##### Returns

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

A completely initialized Chromium engine.

##### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.Create(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref> method
with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling <code>new EngineOptions.Builder().Build()</code>.

##### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

#### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync"></a> CreateAsync\(\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)\>

A task which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

##### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.CreateAsync(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling <code>new EngineOptions.Builder().Build()</code>.

#### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync_DotNetBrowser_Engine_EngineOptions_"></a> CreateAsync\(EngineOptions\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync(EngineOptions options)
```

##### Parameters

`options` [EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

The <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance that will be used for initializing the engine

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)\>

A task which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

##### Examples

<pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = await EngineFactory.CreateAsync(engineOptions);</code></pre>

##### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

Native keyboard input is enabled with hardware-accelerated rendering on Windows or Linux.

#### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync_DotNetBrowser_Engine_RenderingMode_"></a> CreateAsync\(RenderingMode\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync(RenderingMode renderingMode)
```

##### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

The <xref href="DotNetBrowser.Engine.RenderingMode" data-throw-if-not-resolved="false"></xref> that will be used for initializing the engine

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)\>

A task, which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

##### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.CreateAsync(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling
<code>new EngineOptions.Builder().Build()</code> with the <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> specified.

## <a id="DotNetBrowser_Engine_EngineInitializationException"></a> Class EngineInitializationException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The base class for those exceptions that can be thrown during <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization.

```csharp
public class EngineInitializationException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException)

##### Derived

[AutoDeElevationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_AutoDeElevationException), 
[ChromiumBinariesMissingException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ChromiumBinariesMissingException), 
[LicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_LicenseException), 
[MissingDependencyException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_MissingDependencyException), 
[SandboxNotSupportedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_SandboxNotSupportedException), 
[UserDataCreationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataCreationException), 
[UserDataInUseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataInUseException)

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

#### <a id="DotNetBrowser_Engine_EngineInitializationException__ctor_System_String_"></a> EngineInitializationException\(string\)

Initializes a new instance of the <xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> with the specified
<code class="paramref">message</code>.

```csharp
public EngineInitializationException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

The detail message.

#### <a id="DotNetBrowser_Engine_EngineInitializationException__ctor_System_Int64_"></a> EngineInitializationException\(long\)

Initializes a new instance of the <xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> with the specified
Chromium <code class="paramref">exitCode</code>.

```csharp
public EngineInitializationException(long exitCode)
```

##### Parameters

`exitCode` [long](https://learn.microsoft.com/dotnet/api/system.int64)

The Chromium exit code.

## <a id="DotNetBrowser_Engine_EngineOptions"></a> Class EngineOptions

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The options that are used to configure <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

```csharp
public class EngineOptions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Engine_EngineOptions_BinariesExtractionOptions"></a> BinariesExtractionOptions

Gets the options that are used to configure the Chromium binaries extraction process.

```csharp
public BinariesExtractionOptions BinariesExtractionOptions { get; }
```

##### Property Value

 [BinariesExtractionOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesExtractionOptions)

#### <a id="DotNetBrowser_Engine_EngineOptions_ChromiumDirectory"></a> ChromiumDirectory

Gets the absolute path to the directory where the Chromium binaries are located.

```csharp
public string ChromiumDirectory { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    If the directory contains the Chromium binaries, the library will check them and make
    sure that they are compatible with the current library version. If the directory does not
    contain the Chromium binaries, or the binaries aren't compatible with the current library
    version, the library will search for the binaries inside the assemblies from the application
    references and working directory and extract them into the given directory programmatically.
    It might take some time to extract the Chromium binaries from a JAR archive. The time depends on the hardware
    (CPU and SSD/HDD) performance.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_ChromiumSwitches"></a> ChromiumSwitches

Gets an immutable collection of the Chromium switches that will be passed to the Chromium Main
process.

```csharp
public IEnumerable<string> ChromiumSwitches { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Remarks

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

#### <a id="DotNetBrowser_Engine_EngineOptions_CrashDumpDirectory"></a> CrashDumpDirectory

Gets the path that will be used to store the automatically generated Chromium crash dumps.

```csharp
public string CrashDumpDirectory { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Engine_EngineOptions_DiskCacheSize"></a> DiskCacheSize

Gets the disk cache size.

```csharp
public long DiskCacheSize { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

##### Remarks

If the disk cache size was not set, then it will be calculated automatically. The size
depends on the available disk space in the volume where the disk cache is located.

#### <a id="DotNetBrowser_Engine_EngineOptions_GoogleApiKey"></a> GoogleApiKey

Gets the Google API key.

```csharp
public string GoogleApiKey { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_GoogleDefaultClientId"></a> GoogleDefaultClientId

Gets the Google client ID.

```csharp
public string GoogleDefaultClientId { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_GoogleDefaultClientSecret"></a> GoogleDefaultClientSecret

Gets the Google client secret.

```csharp
public string GoogleDefaultClientSecret { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_IsAutoplayEnabled"></a> IsAutoplayEnabled

Indicates whether video playback will automatically start after page loading.

```csharp
public bool IsAutoplayEnabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsDnsOverHttpsDisabled"></a> IsDnsOverHttpsDisabled

Indicates whether the DNS over HTTPS (DoH) protocol is disabled.

```csharp
public bool IsDnsOverHttpsDisabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsFileAccessFromFilesAllowed"></a> IsFileAccessFromFilesAllowed

Indicates whether file access from files is allowed.

```csharp
public bool IsFileAccessFromFilesAllowed { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsGpuDisabled"></a> IsGpuDisabled

Indicates whether GPU is disabled.

```csharp
public bool IsGpuDisabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsIncognitoEnabled"></a> IsIncognitoEnabled

Indicates whether the incognito mode for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance is enabled.

```csharp
public bool IsIncognitoEnabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

In the incognito mode the user data such as browsing history, cookies, site data, and the
information entered in forms are stored in memory and released once you close the <code>Engine</code>.

#### <a id="DotNetBrowser_Engine_EngineOptions_IsMediaRoutingEnabled"></a> IsMediaRoutingEnabled

Indicates whether media routing is enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

<p>
    By default, it is disabled.
</p>

```csharp
public bool IsMediaRoutingEnabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsNativeKeyboardInputEnabled"></a> IsNativeKeyboardInputEnabled

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

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsSandboxDisabled"></a> IsSandboxDisabled

Indicates whether the sandbox is disabled.

```csharp
public bool IsSandboxDisabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsTouchMenuDisabled"></a> IsTouchMenuDisabled

Indicates whether touch popup menu is disabled.

```csharp
public bool IsTouchMenuDisabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_IsWebSecurityDisabled"></a> IsWebSecurityDisabled

Indicates whether the same-origin policy is disabled.

```csharp
public bool IsWebSecurityDisabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Language"></a> Language

Gets the Chromium language that is used on the default error pages and message dialogs.

```csharp
public Language Language { get; }
```

##### Property Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

##### Remarks

<p>
    By default, the language is dynamically configured according to the default locale of the
    application. If the list of supported languages does not contain the language obtained from
    the application locale, then the US English language is used.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_LicenseKey"></a> LicenseKey

Gets the license key.

```csharp
public string LicenseKey { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

The license key can be set via adding the "dotnetbrowser.license" file as embedded resource or individually
for every <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> using the <xref href="DotNetBrowser.Engine.EngineOptions.LicenseKey" data-throw-if-not-resolved="false"></xref> property.

#### <a id="DotNetBrowser_Engine_EngineOptions_PasswordStore"></a> PasswordStore

Gets the password store type which specifies the
storage backend should be used to encrypt cookies on Linux.

```csharp
public PasswordStore PasswordStore { get; }
```

##### Property Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

##### Remarks

If the password store type was not set, then the encryption storage backend is chosen by
Chromium engine automatically.

#### <a id="DotNetBrowser_Engine_EngineOptions_ProprietaryFeatures"></a> ProprietaryFeatures

Gets the proprietary features enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public ProprietaryFeatures ProprietaryFeatures { get; }
```

##### Property Value

 [ProprietaryFeatures](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ProprietaryFeatures)

#### <a id="DotNetBrowser_Engine_EngineOptions_RemoteDebuggingPort"></a> RemoteDebuggingPort

Gets the remote debugging port.

```csharp
public uint RemoteDebuggingPort { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

##### Remarks

<p>
    This option enables remote debugging over HTTP at the specific port. When remote
    debugging is enabled, you can navigate to the <code>http://localhost:&lt;port&gt;</code> address from
    another <code>Browser</code> instance or from the Google Chrome browser and debug the loaded web
    pages using Chrome DevTools. If you use Google Chrome browser for remote debugging, its
    version must be equal to the Chromium engine version that is used in DotNetBrowser.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_RenderingMode"></a> RenderingMode

Gets the rendering mode indicating how the content of the web pages will be rendered.

```csharp
public RenderingMode RenderingMode { get; }
```

##### Property Value

 [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

#### <a id="DotNetBrowser_Engine_EngineOptions_Schemes"></a> Schemes

Gets the readonly dictionary of the schemes that will be intercepted.

```csharp
public IReadOnlyDictionary<Scheme, IHandler<InterceptRequestParameters, InterceptRequestResponse>> Schemes { get; }
```

##### Property Value

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme), [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[InterceptRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestParameters), [InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)\>\>

#### <a id="DotNetBrowser_Engine_EngineOptions_UserAgent"></a> UserAgent

Gets the custom user agent string that is used to override the default user agent for the
<xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
public string UserAgent { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Engine_EngineOptions_UserAgentMetadata"></a> UserAgentMetadata

Override profile client hints engine-wide.

```csharp
public UserAgentMetadata UserAgentMetadata { get; }
```

##### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

#### <a id="DotNetBrowser_Engine_EngineOptions_UserDataDirectory"></a> UserDataDirectory

Gets an absolute path to the directory where the user data is stored.

```csharp
public string UserDataDirectory { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    The user data directory stores the data such as cache, cookies, history, GPU cache, local
    storage, visited links, web data, spell checking dictionary files, etc.
</p>
<p>
    <b>Important</b>: the user data directory cannot be used at the same time by multiple <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>
    instances running in a single or different applications.
</p>

### Methods

#### <a id="DotNetBrowser_Engine_EngineOptions_IsProprietaryFeatureEnabled_DotNetBrowser_Engine_ProprietaryFeatures_"></a> IsProprietaryFeatureEnabled\(ProprietaryFeatures\)

Checks whether the given proprietary features are enabled.

```csharp
public bool IsProprietaryFeatureEnabled(ProprietaryFeatures proprietaryFeatures)
```

##### Parameters

`proprietaryFeatures` [ProprietaryFeatures](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ProprietaryFeatures)

the features to check.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the feature is enabled, false otherwise.

## <a id="DotNetBrowser_Engine_EngineOptions_Builder"></a> Class EngineOptions.Builder

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct engine options.

```csharp
public class EngineOptions.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineOptions.Builder](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions_Builder)

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

### Properties

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_AutoplayEnabled"></a> AutoplayEnabled

Enables or disables automatic video playback after page loading.

```csharp
public bool AutoplayEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_BinariesExtractionOptions"></a> BinariesExtractionOptions

Gets or sets the options that are used to configure the Chromium binaries extraction process.

```csharp
public BinariesExtractionOptions BinariesExtractionOptions { get; set; }
```

##### Property Value

 [BinariesExtractionOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_BinariesExtractionOptions)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ChromiumDirectory"></a> ChromiumDirectory

Gets or sets the absolute path to the directory where Chromium binaries are located or the empty
string if it was not set.

```csharp
public string ChromiumDirectory { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    If the directory contains the Chromium binaries, the library will check them and make
    sure that they are compatible with the current library version. If the directory does not
    contain the Chromium binaries, or the binaries aren't compatible with the current library
    version, the library will search for the binaries inside the assemblies from the application
    references and working directory and extract them into the given directory programmatically.
    It might take some time to extract the Chromium binaries from a JAR archive. The time depends on the hardware
    (CPU and SSD/HDD) performance.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ChromiumSwitches"></a> ChromiumSwitches

Gets a set of the Chromium switches that will be passed to the Chromium Main
process.

```csharp
public HashSet<string> ChromiumSwitches { get; }
```

##### Property Value

 [HashSet](https://learn.microsoft.com/dotnet/api/system.collections.generic.hashset\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Remarks

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

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_CrashDumpDirectory"></a> CrashDumpDirectory

Gets or sets the path that will be used to store automatically generated Chromium crash dumps.

```csharp
public string CrashDumpDirectory { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

If this property is set to null, the default path will be used. If this property is set to an empty string,
crash dump generation will be disabled.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_DiskCacheSize"></a> DiskCacheSize

Gets or sets the disk cache size.

```csharp
public long DiskCacheSize { get; set; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

##### Remarks

If the disk cache size was not set, then it will be calculated automatically. The size
depends on the available disk space in the volume where the disk cache is located.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_DnsOverHttpsDisabled"></a> DnsOverHttpsDisabled

Disables the DNS over HTTPS (DoH) protocol.

```csharp
public bool DnsOverHttpsDisabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

<p>
    By default, DoH is enabled.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_FileAccessFromFilesAllowed"></a> FileAccessFromFilesAllowed

Allows or disallows the file access from files.

```csharp
public bool FileAccessFromFilesAllowed { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleApiKey"></a> GoogleApiKey

Gets or sets the Google API key.

```csharp
public string GoogleApiKey { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleDefaultClientId"></a> GoogleDefaultClientId

Gets or sets the Google client ID.

```csharp
public string GoogleDefaultClientId { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GoogleDefaultClientSecret"></a> GoogleDefaultClientSecret

Gets or sets the Google client secret.

```csharp
public string GoogleDefaultClientSecret { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    Some Chromium features such as Geolocation, Spelling, Speech, etc. use Google APIs, and
    to access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required.
    Setting up API keys is optional. If you do not do it, the specific APIs using Google services
    won't work.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_GpuDisabled"></a> GpuDisabled

Disables or enables GPU.

```csharp
public bool GpuDisabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_IncognitoEnabled"></a> IncognitoEnabled

Enables or disables the incognito mode for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public bool IncognitoEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Remarks

In the incognito mode the user data such as browsing history, cookies, site data, and the
information entered in forms are stored in memory and released once you close the <code>Engine</code>.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Language"></a> Language

Gets or sets the Chromium language that is used on the default error pages and message dialogs.

```csharp
public Language Language { get; set; }
```

##### Property Value

 [Language](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Language)

##### Remarks

<p>
    By default, the language is dynamically configured according to the default locale of the
    application. If the list of supported languages does not contain the language obtained from
    the application locale, then the US English language is used. This property allows you
    to override the default behavior and configure the Chromium engine with the given language.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_LicenseKey"></a> LicenseKey

Gets or sets the license key.

```csharp
public string LicenseKey { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

The license key can be set via adding the "dotnetbrowser.license" file as embedded resource or individually
for every <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> using the <xref href="DotNetBrowser.Engine.EngineOptions.Builder.LicenseKey" data-throw-if-not-resolved="false"></xref> property.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_MediaRoutingEnabled"></a> MediaRoutingEnabled

Enables or disables the media routing.

<p>
    By default, it is disabled.
</p>

```csharp
public bool MediaRoutingEnabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_NativeKeyboardInputEnabled"></a> NativeKeyboardInputEnabled

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

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_PasswordStore"></a> PasswordStore

Gets or sets the password store type which specifies the
storage backend should be used to encrypt cookies on Linux.

```csharp
public PasswordStore PasswordStore { get; set; }
```

##### Property Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

##### Remarks

If the password store type was not set, then the encryption storage backend is chosen by
Chromium engine automatically.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_ProprietaryFeatures"></a> ProprietaryFeatures

Gets or sets the proprietary features enabled for the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.
By default, all the proprietary features are disabled.

```csharp
public ProprietaryFeatures ProprietaryFeatures { get; set; }
```

##### Property Value

 [ProprietaryFeatures](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ProprietaryFeatures)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_RemoteDebuggingPort"></a> RemoteDebuggingPort

Gets or sets the remote debugging port.

```csharp
public uint RemoteDebuggingPort { get; set; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

##### Remarks

<p>
    This option enables remote debugging over HTTP at the specific port. When remote
    debugging is enabled, you can navigate to the <code>http://localhost:&lt;port&gt;</code> address from
    another <code>Browser</code> instance or from the Google Chrome browser and debug the loaded web
    pages using Chrome DevTools. If you use Google Chrome browser for remote debugging, its
    version must be equal to the Chromium engine version that is used in DotNetBrowser.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_RenderingMode"></a> RenderingMode

Gets or sets the rendering mode indicating how the content of the web pages will be rendered.

```csharp
public RenderingMode RenderingMode { get; set; }
```

##### Property Value

 [RenderingMode](DotNetBrowser.Engine.md#DotNetBrowser_Engine_RenderingMode)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_SandboxDisabled"></a> SandboxDisabled

Enables or disables the sandbox.

```csharp
public bool SandboxDisabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Schemes"></a> Schemes

Gets the dictionary of the schemes that will be intercepted.

```csharp
public IDictionary<Scheme, IHandler<InterceptRequestParameters, InterceptRequestResponse>> Schemes { get; }
```

##### Property Value

 [IDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2)<[Scheme](DotNetBrowser.Net.md#DotNetBrowser_Net_Scheme), [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[InterceptRequestParameters](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestParameters), [InterceptRequestResponse](DotNetBrowser.Net.Handlers.md#DotNetBrowser_Net_Handlers_InterceptRequestResponse)\>\>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_TouchMenuDisabled"></a> TouchMenuDisabled

Enables or disables the touch popup menu.

```csharp
public bool TouchMenuDisabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserAgent"></a> UserAgent

Gets or sets the custom user agent string that is used to override the default user agent for the
<xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
public string UserAgent { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

This property has the same effect as adding the <code>--user-agent</code> switch.

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserAgentMetadata"></a> UserAgentMetadata

Override profile client hints engine-wide.

```csharp
public UserAgentMetadata UserAgentMetadata { get; set; }
```

##### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.md#DotNetBrowser_Browser_UserAgentMetadata)

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_UserDataDirectory"></a> UserDataDirectory

Gets or sets an absolute path to the directory where the user data is stored.

```csharp
public string UserDataDirectory { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    The user data directory stores the data such as cache, cookies, history, GPU cache, local
    storage, visited links, web data, spell checking dictionary files, etc.
</p>
<p>
    <b>Important</b>: the user data directory cannot be used at the same time by multiple <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>
    instances running in a single or different applications.
</p>

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_WebSecurityDisabled"></a> WebSecurityDisabled

Enables or disables the same-origin policy.

```csharp
public bool WebSecurityDisabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### Methods

#### <a id="DotNetBrowser_Engine_EngineOptions_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public EngineOptions Build()
```

##### Returns

 [EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

new <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

## <a id="DotNetBrowser_Engine_InvalidLicenseException"></a> Class InvalidLicenseException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the given license is invalid.

```csharp
public sealed class InvalidLicenseException : LicenseException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[LicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_LicenseException) ← 
[InvalidLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_InvalidLicenseException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Engine_InvalidLicenseException__ctor_System_String_System_String_"></a> InvalidLicenseException\(string, string\)

```csharp
public InvalidLicenseException(string message, string helpLink = null)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

`helpLink` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Engine_LicenseException"></a> Class LicenseException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The base class for those exceptions that can be thrown during license checking.

```csharp
public class LicenseException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[LicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_LicenseException)

##### Derived

[InvalidLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_InvalidLicenseException), 
[NoLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_NoLicenseException)

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

#### <a id="DotNetBrowser_Engine_LicenseException__ctor_System_String_"></a> LicenseException\(string\)

Initializes a new instance of the <xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> with the specified
<code class="paramref">message</code>.

```csharp
public LicenseException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

The detail message.

## <a id="DotNetBrowser_Engine_MissingDependencyException"></a> Class MissingDependencyException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when Chromium fails to find the required system libraries on Linux.

```csharp
public sealed class MissingDependencyException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[MissingDependencyException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_MissingDependencyException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    When this exception is thrown, the following actions should be performed:<br />
    - make sure that the current Linux distribution and version meets the
    <a href="https://teamdev.com/dotnetbrowser/docs/guides/requirements.html">https://teamdev.com/dotnetbrowser/docs/guides/requirements.html</a>
    system requirements <br />
    - install the required system libraries
</p>

## <a id="DotNetBrowser_Engine_NoLicenseException"></a> Class NoLicenseException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when no license found.

```csharp
public class NoLicenseException : LicenseException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[LicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_LicenseException) ← 
[NoLicenseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_NoLicenseException)

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

#### <a id="DotNetBrowser_Engine_NoLicenseException__ctor"></a> NoLicenseException\(\)

```csharp
public NoLicenseException()
```

## <a id="DotNetBrowser_Engine_PasswordStore"></a> Class PasswordStore

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Defines password store types that are used to specify which encryption storage backend to use to
encrypt cookies on Linux.

```csharp
public sealed class PasswordStore : TypedEnum<string>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
TypedEnum<string\> ← 
[PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Engine_PasswordStore_Auto"></a> Auto

Choose encryption automatically.

```csharp
public static readonly PasswordStore Auto
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_Basic"></a> Basic

Use basic encryption.

```csharp
public static readonly PasswordStore Basic
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_Default"></a> Default

Default password store encryption (Auto).

```csharp
public static readonly PasswordStore Default
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_Gnome"></a> Gnome

Use GNOME encryption.

```csharp
public static readonly PasswordStore Gnome
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_GnomeKeyring"></a> GnomeKeyring

Use GNOME keyring encryption.

```csharp
public static readonly PasswordStore GnomeKeyring
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_GnomeLibsecret"></a> GnomeLibsecret

Use GNOME libsecret encryption.

```csharp
public static readonly PasswordStore GnomeLibsecret
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_KWallet"></a> KWallet

Use KWallet encryption.

```csharp
public static readonly PasswordStore KWallet
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

#### <a id="DotNetBrowser_Engine_PasswordStore_KWallet5"></a> KWallet5

Use KWallet5 encryption.

```csharp
public static readonly PasswordStore KWallet5
```

##### Field Value

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

### Operators

#### <a id="DotNetBrowser_Engine_PasswordStore_op_Explicit_System_String__DotNetBrowser_Engine_PasswordStore"></a> explicit operator PasswordStore\(string\)

Returns the <xref href="DotNetBrowser.Engine.PasswordStore" data-throw-if-not-resolved="false"></xref> instance by its string representation.

```csharp
public static explicit operator PasswordStore(string value)
```

##### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The password store string representation

##### Returns

 [PasswordStore](DotNetBrowser.Engine.md#DotNetBrowser_Engine_PasswordStore)

The <xref href="DotNetBrowser.Engine.PasswordStore" data-throw-if-not-resolved="false"></xref> instance that corresponds to the provided string representation.

## <a id="DotNetBrowser_Engine_SandboxNotSupportedException"></a> Class SandboxNotSupportedException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the current environment does not support creating processes within a new user namespace,
preventing Chromium from being launched in sandbox mode.

```csharp
public sealed class SandboxNotSupportedException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[SandboxNotSupportedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_SandboxNotSupportedException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    When this exception is thrown, consider disabling the sandbox mode via
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.SandboxDisabled" data-throw-if-not-resolved="false"></xref> property or by adding the
    <code>--no-sandbox</code> switch to <xref href="DotNetBrowser.Engine.EngineOptions.Builder.ChromiumSwitches" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    For more information, see
    <a href="https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox">https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox</a>.
</p>

## <a id="DotNetBrowser_Engine_UserDataCreationException"></a> Class UserDataCreationException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the user data directory cannot be created.

```csharp
public sealed class UserDataCreationException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[UserDataCreationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataCreationException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    This exception indicates that the Chromium engine failed to create the user data directory.
    This can happen due to:<br />
    - insufficient permissions to create the directory, or<br />
    - the path is invalid or inaccessible.
</p>
<p>
    To resolve this issue:<br />
    - ensure the application has write permissions to the parent directory, or<br />
    - specify a different user data directory via
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.UserDataDirectory" data-throw-if-not-resolved="false"></xref> property.
</p>

### Properties

#### <a id="DotNetBrowser_Engine_UserDataCreationException_UserDataDirectory"></a> UserDataDirectory

Gets the user data directory path that could not be created.

```csharp
public string UserDataDirectory { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Engine_UserDataInUseException"></a> Class UserDataInUseException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the user data directory is already in use by another Chromium engine instance.

```csharp
public sealed class UserDataInUseException : EngineInitializationException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineInitializationException) ← 
[UserDataInUseException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_UserDataInUseException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Remarks

<p>
    This exception indicates that another instance of the Chromium engine is currently using
    the same user data directory. Each Chromium engine instance requires exclusive access
    to its user data directory.
</p>
<p>
    To resolve this issue, either:<br />
    - close the other instance using the same user data directory, or<br />
    - specify a different user data directory via
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.UserDataDirectory" data-throw-if-not-resolved="false"></xref> property.
</p>

### Properties

#### <a id="DotNetBrowser_Engine_UserDataInUseException_UserDataDirectory"></a> UserDataDirectory

Gets the user data directory path that is already in use.

```csharp
public string UserDataDirectory { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Engine_IEngine"></a> Interface IEngine

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Provides access to the Chromium engine functionality.

```csharp
public interface IEngine : IDisposable, IAutoDisposable<EngineDisposedEventArgs>, IAutoDisposable
```

##### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable<EngineDisposedEventArgs\>](DotNetBrowser.md#DotNetBrowser_IAutoDisposable_1), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Remarks

<p>
    To perform operations with the engine, a license key is required. The license key represents
    a string that can be set via the <code>dotnetbrowser.license</code> file or individually for every
    <code>IEngine</code> using the <xref href="DotNetBrowser.Engine.EngineOptions.LicenseKey?text=LicenseKey" data-throw-if-not-resolved="false"></xref> property. If you
    set the license key via configuring the license file, then please make sure that you set it
    before creating an <code>IEngine</code> instance.
</p>
<p>
    The Chromium engine is running in a separate native process. Communication between the native
    and .NET process is done through the Inter-Process Communication (IPC) layer that allows
    transferring data between two processes on a local machine.
</p>
<p>
    The native process allocates memory and system resources that must be released. So, when the
    engine is no longer needed, it must be disposed through the <xref href="System.IDisposable.Dispose" data-throw-if-not-resolved="false"></xref> method to
    shutdown the native process and free all the allocated memory and system resources. For example:
</p>

<pre><code class="lang-csharp">IEngine engine = EngineFactory.Create(engineOptions);
//...
engine.Dispose();</code></pre>

<p>
    Any attempt to use an already disposed engine or any of its services will lead to the
    <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    To get notifications that the <code>IEngine</code> instance has been disposed subscribe to the
    following event:
</p>

<pre><code class="lang-csharp">engine.Disposed += (s, e) =&gt; {
// The engine has been disposed or unexpectedly crashed.
};</code></pre>

<p>To get notifications that the <code>IEngine</code> instance has been unexpectedly crashed use:</p>

<pre><code class="lang-csharp">engine.Disposed += (s, e) =&gt; {
    long exitCode = e.ExitCode;
    // The engine has been crashed if this exit code is non-zero.
};</code></pre>

<example>

    <pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = EngineFactory.Create(engineOptions);</code></pre>

</example>

### Properties

#### <a id="DotNetBrowser_Engine_IEngine_MediaDevices"></a> MediaDevices

Gets the service that allows managing media stream devices.

```csharp
IMediaDevices MediaDevices { get; }
```

##### Property Value

 [IMediaDevices](DotNetBrowser.Media.md#DotNetBrowser_Media_IMediaDevices)

#### <a id="DotNetBrowser_Engine_IEngine_Options"></a> Options

Gets the options that were used to initialize this <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
EngineOptions Options { get; }
```

##### Property Value

 [EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions)

#### <a id="DotNetBrowser_Engine_IEngine_Profiles"></a> Profiles

Gets the live collection of the Chromium profiles available in this engine.

```csharp
IProfiles Profiles { get; }
```

##### Property Value

 [IProfiles](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfiles)

#### <a id="DotNetBrowser_Engine_IEngine_Theme"></a> Theme

Gets or sets the current Chromium theme.

```csharp
Theme Theme { get; set; }
```

##### Property Value

 [Theme](DotNetBrowser.Engine.md#DotNetBrowser_Engine_Theme)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Engine_IEngine_Widevine"></a> Widevine

Gets the service that allows activating the Widevine component for DRM content playback.

```csharp
IWidevine Widevine { get; }
```

##### Property Value

 [IWidevine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IWidevine)

### Methods

#### <a id="DotNetBrowser_Engine_IEngine_CreateBrowser"></a> CreateBrowser\(\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page.

```csharp
IBrowser CreateBrowser()
```

##### Returns

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

The new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

##### Remarks

This browser instance will be bound to the default Chromium profile.

## <a id="DotNetBrowser_Engine_IWidevine"></a> Interface IWidevine

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The Widevine DRM (Digital Rights Management) component.

```csharp
public interface IWidevine
```

### Remarks

<p>
    Widevine is used to protect digital content and ensure that it is accessed and used in
    compliance with licensing agreements.
</p>
<p>
    To use Widevine, you must activate it every time you create a new
    <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance. By default, Widevine is not activated. Once activated, you can play protected
    content such as Netflix, Amazon Prime Video, etc. in the browsers of the engine.
</p>
<p>The Widevine component files are stored in the user data directory of the engine.</p>
<p>
    On Windows and macOS, you can activate Widevine without specifying a custom user data
    directory. There's no need to restart the engine after first activation or update, as the changes
    are applied automatically.
</p>
<p>
    On Linux, you must specify a custom user data directory to activate Widevine. It is required
    due to the way Widevine is implemented on Linux. When the component is activated for the first
    time, or it is updated to the latest version during activation, the engine must be restarted to
    apply the changes. To find out if the restart is required, check the activation status:
</p>

<pre><code class="lang-csharp">var status = engine.Widevine.Activate().Result;
if (status == WidevineActivationStatus.RestartRequired)
{
    // Engine restart is required.
}</code></pre>

<p>
    <b>Important</b>: Widevine is a Google proprietary component, governed by its own terms
    of use. For more information, see
    <a href="https://www.widevine.com/">https://www.widevine.com/</a>.
    TeamDev shall not be responsible for your use of Widevine.
</p>

### Properties

#### <a id="DotNetBrowser_Engine_IWidevine_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance that this Widevine service belongs to.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Engine_IWidevine_IsActivated"></a> IsActivated

Indicates whether Widevine is activated.

```csharp
bool IsActivated { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

### Methods

#### <a id="DotNetBrowser_Engine_IWidevine_Activate"></a> Activate\(\)

Activates the Widevine component and updates it to the latest version if it is available.

```csharp
Task<WidevineActivationStatus> Activate()
```

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[WidevineActivationStatus](DotNetBrowser.Engine.md#DotNetBrowser_Engine_WidevineActivationStatus)\>

The task that completes with the status of the Widevine activation.

##### Remarks

<p>The Widevine component files are stored in the user data directory of the engine.</p>
<p>
    On Windows and macOS, you can activate Widevine without specifying a custom user data
    directory. There's no need to restart the engine after first activation or update, as the
    changes are applied automatically.
</p>
<p>
    On Linux, you must specify a custom user data directory to activate Widevine. It is
    required due to the way Widevine is implemented on Linux. When the component is activated
    for the first time, or it is updated to the latest version during activation, the engine
    must be restarted to apply the changes.
</p>
<p>
    Here is an example of how to specify a custom user data directory and restart the engine
    if it is required:
</p>

<pre><code class="lang-csharp">var options = new EngineOptions.Builder()
{
    // Specify a custom user data directory.
    UserDataDirectory = "path/to/user/data/dir"
}.Build();
var engine = EngineFactory.Create(options);
// Activate Widevine and restart the engine if necessary.
var status = engine.Widevine.Activate().Result;
if (status == WidevineActivationStatus.RestartRequired)
{
    // Restart the engine with the same options.
    engine.Dispose();
    engine = EngineFactory.Create(options);
}
var browser = engine.CreateBrowser();</code></pre>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

##### See Also

[EngineOptions](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions).[Builder](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions_Builder).[UserDataDirectory](DotNetBrowser.Engine.md#DotNetBrowser_Engine_EngineOptions_Builder_UserDataDirectory)

## <a id="DotNetBrowser_Engine_BinariesVerificationLevel"></a> Enum BinariesVerificationLevel

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The level of the Chromium binaries verification.

```csharp
public enum BinariesVerificationLevel
```

### Fields

`Minimal = 1` 

Check files presence only.



`Normal = 2` 

Check files presence and size.



`Off = 0` 

Do not perform binaries verification.



`Strong = 3` 

Check files presence and hash.

Calculating hash is a time-consuming operation, so this check slows down the engine initialization.

## <a id="DotNetBrowser_Engine_ProprietaryFeatures"></a> Enum ProprietaryFeatures

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The list of supported proprietary features.

```csharp
[Flags]
public enum ProprietaryFeatures
```

### Fields

`Aac = 64` 

<p>Represents support of the AAC codec.</p>
<p>
    <b>Important</b>: AAC codec is a proprietary component. By enabling this codec you
    state that you are aware that AAC is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of AAC codec.
</p>



`H264 = 1` 

<p>Represents support of the H.264 codec.</p>
<p>
    <b>Important</b>: H.264 codec is a proprietary component. By enabling this codec you
    state that you are aware that H.264 is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of H.264 codec.
</p>



`Hevc = 16` 

<p>Represents support of the HEVC codec.</p>
<p>
    <b>Important</b>: HEVC codec is a proprietary component. By enabling this codec you
    state that you are aware that HEVC is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of HEVC codec.
</p>



`None = 0` 

No proprietary features enabled.

## <a id="DotNetBrowser_Engine_RenderingMode"></a> Enum RenderingMode

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The supported rendering modes.

```csharp
public enum RenderingMode
```

### Fields

`HardwareAccelerated = 1` 

The engine renders content using GPU and displays it directly on a native surface (window).



`OffScreen = 2` 

The engine renders content using GPU and copies the pixels to the process memory.

## <a id="DotNetBrowser_Engine_Theme"></a> Enum Theme

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The Chromium theme, which affects the appearanceof web pages and their contents,
as well as Chromium dialogs, such as Print Preview and DevTools.

```csharp
public enum Theme
```

### Fields

`Dark = 2` 

The dark theme.



`Light = 1` 

The light theme.



`System = 3` 

The theme inherited from the operating system settings.

## <a id="DotNetBrowser_Engine_WidevineActivationStatus"></a> Enum WidevineActivationStatus

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Represents the result of attempting to activate the Widevine component.

```csharp
public enum WidevineActivationStatus
```

### Fields

`Activated = 1` 

The Widevine component is successfully activated and updated to the latest version.



`ActivationFailed = 3` 

Activation of the Widevine component has failed.

Activation can fail due to various reasons, such as network issues or some internal
errors on the remote service.

`NotSupported = 4` 

The Widevine component is not supported on the current platform and CPU architecture.



`RestartRequired = 2` 

The Widevine component is successfully activated, but the engine restart is required to
start using it.

This status is used on Linux only, because the engine cannot start using it right after
activation or updating to the latest version.
