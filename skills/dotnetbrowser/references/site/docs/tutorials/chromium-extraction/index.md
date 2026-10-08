
# Pre-extracting Chromium Binaries

**Lead**
This article explains how to extract DotNetBrowser Chromium binaries as part of
a .NET build or publish workflow.


Use the `DotNetBrowser.Chromium.Extraction` NuGet package in .NET applications
that use DotNetBrowser.

If you also need to apply white-label branding such as executable names,
icons, or macOS bundle metadata, see [Branding Chromium binaries](https://teamdev.com/dotnetbrowser/docs/tutorials/chromium-branding/).

DotNetBrowser deploys Chromium binaries together with the library. In most
applications, DotNetBrowser extracts and uses these binaries automatically. The
package described here is useful when you need more control over the build,
publish, and deployment pipeline:

* `DotNetBrowser.Chromium.Extraction` extracts DotNetBrowser Chromium binaries
  during `dotnet build` or `dotnet publish`.

This package is configured through MSBuild properties in the application
project file.

## Prerequisites

Before you start, make sure that your application project references the
DotNetBrowser API package and a platform-specific Chromium package that matches
the target runtime. The API package provides the .NET APIs used by the
application, while the Chromium package provides the corresponding Chromium
binaries that the extraction tool processes.

For the complete list of supported packages and platform-specific installation
options, see [Installing from NuGet](https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/).

**Important**
Run extraction on the same operating system family as the target runtime. For
example, extract Linux binaries on Linux and macOS binaries on macOS. This
preserves executable permissions, symbolic links, and platform bundle
structure.


## DotNetBrowser.Chromium.Extraction

`DotNetBrowser.Chromium.Extraction` is an MSBuild task package that extracts
Chromium binaries from platform-specific `DotNetBrowser.Chromium.*.dll`
assemblies.

Use this package when you need unpacked Chromium binaries as part of your build,
publish, deployment, container image, or CI/CD artifact.

The package uses a `DotNetBrowser.Chromium.*.dll` assembly that contains
compressed Chromium binaries.

### Install DotNetBrowser.Chromium.Extraction

Add the package to your application project:

```xml
<ItemGroup>
  <PackageReference Include="DotNetBrowser.Chromium.Extraction"
                    Version="..."
                    PrivateAssets="all" />
</ItemGroup>
```

`PrivateAssets="all"` keeps the build helper package private to your project.
It is recommended for application projects because this package provides MSBuild
tasks rather than runtime APIs that should flow transitively to downstream
consumers.

### Extract during build

To extract Chromium binaries after the `Build` target, add the following
properties:

```xml
<PropertyGroup>
  <DotNetBrowserExtractionEnabled>true</DotNetBrowserExtractionEnabled>
  <DotNetBrowserExtractionDuringBuild>true</DotNetBrowserExtractionDuringBuild>
</PropertyGroup>
```

Then build the project:

```powershell
dotnet build -c Release
```

By default, build-time extraction uses:

* source: `$(OutputPath)`
* destination: `$(TargetDir)unpacked/`

The resolved extraction output path is logged in the MSBuild output as
`DotNetBrowserExtractionBuildOutputPath`.

### Extract during publish

To extract Chromium binaries after the `Publish` target, enable publish-time
extraction:

```xml
<PropertyGroup>
  <DotNetBrowserExtractionEnabled>true</DotNetBrowserExtractionEnabled>
  <DotNetBrowserExtractionDuringPublish>true</DotNetBrowserExtractionDuringPublish>
</PropertyGroup>
```

Then publish the application:

```powershell
dotnet publish -c Release -r win-x64
```

By default, publish-time extraction uses:

* source: `$(PublishDir)`
* destination: `$(PublishDir)unpacked/`

The resolved extraction output path is logged in the MSBuild output as
`DotNetBrowserExtractionPublishOutputPath`.

### Configure the extraction source and destination

You can explicitly specify the source and destination paths:

```xml
<PropertyGroup>
  <DotNetBrowserExtractionEnabled>true</DotNetBrowserExtractionEnabled>
  <DotNetBrowserExtractionDuringPublish>true</DotNetBrowserExtractionDuringPublish>
  <DotNetBrowserExtractionSourcePath>$(PublishDir)</DotNetBrowserExtractionSourcePath>
  <DotNetBrowserExtractionDestinationPath>chromium</DotNetBrowserExtractionDestinationPath>
</PropertyGroup>
```

The extraction task appends a platform-specific subdirectory when appropriate,
for example, `WindowsX64`, `LinuxArm64`, `MacX64`, etc.

### Extraction properties


| Property | Default value | Description |
|---|---|---|
| `DotNetBrowserExtractionEnabled` | `false` | Master switch for the extraction targets. |
| `DotNetBrowserExtractionDuringBuild` | `false` | Runs extraction after the `Build` target. |
| `DotNetBrowserExtractionDuringPublish` | `false` | Runs extraction after the `Publish` target. |
| `DotNetBrowserExtractionSourcePath` | Build: `$(OutputPath)`<br/>Publish: `$(PublishDir)` | Source file or directory. It can point to a directory that contains a Chromium assembly. |
| `DotNetBrowserExtractionDestinationPath` | Build: `$(TargetDir)unpacked/`<br/>Publish: `$(PublishDir)unpacked/` | Destination directory for unpacked Chromium binaries. Relative paths are resolved against the build or publish output directory. |


### Runtime identifier and platform resolution

When the extraction source is a directory, the package searches recursively for
`DotNetBrowser.Chromium.*.dll` assemblies. If more than one candidate is found,
the task uses `RuntimeIdentifier` to select the best match.

Supported runtime identifier families include:

* `win-x64`, `win-x86`, `win-arm64`
* `linux-x64`, `linux-arm64`
* `osx-x64`, `osx-arm64`

If `RuntimeIdentifier` is not specified, the task uses the current host
operating system and process architecture.

### Use extracted binaries at application startup

If your deployment pipeline extracts Chromium binaries into a known directory,
configure DotNetBrowser to use that directory via `EngineOptions.ChromiumDirectory`.

The value should point to the base extraction directory. DotNetBrowser appends
the current platform subdirectory automatically.


**C#**
```csharp
string chromiumDirectory = Path.Combine(AppContext.BaseDirectory, "unpacked");

IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumDirectory = chromiumDirectory
}.Build());
```

**VB**
```vb
Dim chromiumDirectory As String =
    Path.Combine(AppContext.BaseDirectory, "unpacked")

Dim engine As IEngine = EngineFactory.Create(
    New EngineOptions.Builder() With {
        .ChromiumDirectory = chromiumDirectory
    }.Build()
)
```



For a publish output where extraction writes to `publish/unpacked/WindowsX64`,
set `ChromiumDirectory` to `publish/unpacked`.
