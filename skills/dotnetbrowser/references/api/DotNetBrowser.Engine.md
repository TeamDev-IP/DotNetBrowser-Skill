# <a id="DotNetBrowser_Engine"></a> Namespace DotNetBrowser.Engine

### Namespaces

 [DotNetBrowser.Engine.Events](DotNetBrowser.Engine.Events.md)

### Classes

 [BinariesExtractionOptions](DotNetBrowser.Engine.BinariesExtractionOptions.md)

The options that are used to configure the Chromium binaries extraction process.

 [EngineOptions.Builder](DotNetBrowser.Engine.EngineOptions.Builder.md)

A builder class to construct engine options.

 [ChromiumBinariesMissingException](DotNetBrowser.Engine.ChromiumBinariesMissingException.md)

Thrown when the engine initialization fails due to missing compatible Chromium binaries.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The exception thrown when the connection to the Chromium engine appears to be closed.

 [EngineFactory](DotNetBrowser.Engine.EngineFactory.md)

Factory class that is used to create <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

 [EngineInitializationException](DotNetBrowser.Engine.EngineInitializationException.md)

The base class for those exceptions that can be thrown during <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization.

 [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

The options that are used to configure <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

 [InvalidLicenseException](DotNetBrowser.Engine.InvalidLicenseException.md)

Thrown when the given license is invalid.

 [LicenseException](DotNetBrowser.Engine.LicenseException.md)

The base class for those exceptions that can be thrown during license checking.

 [MissingDependencyException](DotNetBrowser.Engine.MissingDependencyException.md)

Thrown when Chromium fails to find the required system libraries on Linux.

 [NoLicenseException](DotNetBrowser.Engine.NoLicenseException.md)

Thrown when no license found.

 [PasswordStore](DotNetBrowser.Engine.PasswordStore.md)

Defines password store types that are used to specify which encryption storage backend to use to
encrypt cookies on Linux.

 [SandboxNotSupportedException](DotNetBrowser.Engine.SandboxNotSupportedException.md)

Thrown when the current environment does not support creating processes within a new user namespace,
preventing Chromium from being launched in sandbox mode.

 [UserDataCreationException](DotNetBrowser.Engine.UserDataCreationException.md)

Thrown when the user data directory cannot be created.

 [UserDataInUseException](DotNetBrowser.Engine.UserDataInUseException.md)

Thrown when the user data directory is already in use by another Chromium engine instance.

### Interfaces

 [IEngine](DotNetBrowser.Engine.IEngine.md)

Provides access to the Chromium engine functionality.

 [IWidevine](DotNetBrowser.Engine.IWidevine.md)

The Widevine DRM (Digital Rights Management) component.

### Enums

 [BinariesVerificationLevel](DotNetBrowser.Engine.BinariesVerificationLevel.md)

The level of the Chromium binaries verification.

 [ProprietaryFeatures](DotNetBrowser.Engine.ProprietaryFeatures.md)

The list of supported proprietary features.

 [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

The supported rendering modes.

 [Theme](DotNetBrowser.Engine.Theme.md)

The Chromium theme, which affects the appearanceof web pages and their contents,
as well as Chromium dialogs, such as Print Preview and DevTools.

 [WidevineActivationStatus](DotNetBrowser.Engine.WidevineActivationStatus.md)

Represents the result of attempting to activate the Widevine component.

