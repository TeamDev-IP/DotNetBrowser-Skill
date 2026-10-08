
# Branding Chromium Binaries

**Lead**
This article explains how to apply custom branding to DotNetBrowser Chromium
binaries as part of a `dotnet publish` workflow.


Use the `DotNetBrowser.Branding` NuGet package in .NET applications that use
DotNetBrowser.

If you only need unpacked Chromium binaries for build or publish output, see
[Pre-extracting Chromium binaries](https://teamdev.com/dotnetbrowser/docs/tutorials/chromium-extraction/).

DotNetBrowser deploys Chromium binaries together with the library. In most
applications, DotNetBrowser extracts and uses these binaries automatically. The
package described here is useful when you need more control over branding,
deployment, and white-label output:

* `DotNetBrowser.Branding` applies custom branding to DotNetBrowser Chromium
  binaries during `dotnet publish`. It also includes the extraction tasks, so it
  can extract Chromium binaries before applying branding.

This package is configured through MSBuild properties in the application
project file.

## Prerequisites

Before you start, make sure that your application project references the
DotNetBrowser API package and a platform-specific Chromium package that matches
the target runtime. The API package provides the .NET APIs used by the
application, while the Chromium package provides the corresponding Chromium
binaries that the branding tool processes.

For the complete list of supported packages and platform-specific installation
options, see [Installing from NuGet](https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/).

**Important**
Run branding on the same operating system family as the target runtime. For
example, brand Linux binaries on Linux and macOS binaries on macOS. This
preserves executable permissions, symbolic links, and platform bundle
structure.


## DotNetBrowser.Branding

`DotNetBrowser.Branding` is an MSBuild task package that applies custom branding
to DotNetBrowser Chromium binaries during `dotnet publish`.

Use this package when you need white-label Chromium binaries for your
application, for example, to change the executable name, product metadata,
process display name, icons, or macOS bundle information.

The package includes the Chromium extraction tasks internally. If the branding
source is a `DotNetBrowser.Chromium.*.dll` assembly or a publish directory that
contains one, extraction runs before branding.

Internally, `DotNetBrowser.Branding` uses the
[`chromium_branding`](https://github.com/TeamDev-IP/Chromium-Branding) command-line tool. It customizes DotNetBrowser Chromium binaries by changing
platform-specific branding details, such as executable names, process
display names, icons, version information, copyright and product metadata, and
macOS bundle information. It supports Windows, macOS, and Linux Chromium
binaries.

The NuGet package invokes the tool from MSBuild, so you do not need to run
`chromium_branding` manually.

### Install DotNetBrowser.Branding

Add the package to your application project:

```xml
<ItemGroup>
  <PackageReference Include="DotNetBrowser.Branding"
                    Version="..."
                    PrivateAssets="all" />
</ItemGroup>
```

`PrivateAssets="all"` is recommended for application projects because this
package provides build and publish tasks.

### Minimal branding configuration

Create a branding parameters file, for example `branding.params.json`, and
enable branding in the project file:

```xml
<PropertyGroup>
  <DotNetBrowserBrandingEnabled>true</DotNetBrowserBrandingEnabled>
  <DotNetBrowserBrandingParamsFile>$(MSBuildProjectDirectory)/branding.params.json</DotNetBrowserBrandingParamsFile>
</PropertyGroup>
```

Then publish the application:

```powershell
dotnet publish -c Release -r win-x64
```

Branding runs after `Publish`. By default, the package:

* uses `$(PublishDir)` as the branding source;
* extracts Chromium binaries automatically if the source contains a Chromium
  assembly;
* writes branded binaries to `$(PublishDir)branded/`;
* appends a platform-specific subdirectory such as `WindowsX64`, `LinuxX64`,
  `MacX64`, or `MacArm64`.

The final output path is logged as `DotNetBrowserBrandedOutputPath`.

### Branding parameters file

The branding parameters file is a JSON file consumed by the bundled
`chromium_branding` tool.

Example:

```json
{
  "version": "1.2.3",
  "win": {
    "executableName": "myapp",
    "processDisplayName": "My App",
    "legalCopyright": "© 2026 MyCompany",
    "author": "MyCompany",
    "productName": "MyApp",
    "icoPath": "assets/app.ico",
    "signCommand": "echo @@BINARY_PATH@@"
  },
  "mac": {
    "bundle": {
      "name": "MyApp",
      "id": "com.mycompany.myapp"
    },
    "icnsPath": "assets/app.icns",
    "codesignIdentity": "${CODESIGN_IDENTITY}",
    "codesignEntitlements": "assets/entitlements.plist",
    "provisioningProfile": "assets/app.provisionprofile",
    "teamID": "${TEAM_ID}",
    "appleID": "${APPLE_ID}",
    "password": "${PASSWORD}"
  },
  "linux": {
    "executableName": "myapp"
  }
}
```

Relative asset paths, such as `icoPath`, `icnsPath`, and
`codesignEntitlements`, are resolved against the directory that contains
`branding.params.json` by default. You can override the base directory with the
`DotNetBrowserBrandingAssetsBasePath` MSBuild property.

**Note**
Keep secrets such as Apple ID passwords or signing credentials out of the JSON
file. Use environment variables or CI/CD secret variables where possible.


### Supported branding options

The following options are commonly used in `branding.params.json`.

#### Windows


| Option | Description |
|---|---|
| `executableName` | Custom Chromium executable name without the `.exe` extension. |
| `processDisplayName` | Display name shown for the Chromium process. |
| `legalCopyright` | Copyright metadata for Windows binaries. |
| `author` | Company or author metadata. |
| `productName` | Product name metadata. |
| `icoPath` | Path to an `.ico` file. Relative paths are staged automatically by default. |
| `signCommand` | Command used to sign a branded binary. The branding tool replaces placeholders such as `@@BINARY_PATH@@`. |


#### macOS


| Option | Description |
|---|---|
| `bundle.name` | macOS bundle display name. |
| `bundle.id` | macOS bundle identifier, for example `com.company.product`. |
| `icnsPath` | Path to an `.icns` icon file. Relative paths are staged automatically by default. |
| `codesignIdentity` | Code signing identity. |
| `codesignEntitlements` | Path to the entitlements `.plist` file. Relative paths are staged automatically by default. |
| `provisioningProfile` | Optional path to an Apple-signed `.provisionprofile` file. Required when the entitlements file contains `keychain-access-groups`, for example, to support Touch ID. |
| `teamID` | Apple Developer Team ID. |
| `appleID` | Apple ID used by the signing/notarization workflow. |
| `password` | Password or app-specific password used by the signing/notarization workflow. Prefer secrets or environment variables. |


#### Linux


| Option | Description |
|---|---|
| `executableName` | Custom Chromium executable name. |


### Branding properties


| Property | Default value | Description |
|---|---|---|
| `DotNetBrowserBrandingEnabled` | `false` | Enables branding after publish. |
| `DotNetBrowserBrandingParamsFile` | empty | Required when branding is enabled. Path to `branding.params.json`. |
| `DotNetBrowserBrandingSourcePath` | `$(PublishDir)` | Source file or directory used for branding. |
| `DotNetBrowserBrandingDestinationPath` | `$(PublishDir)branded/` | Output directory for branded binaries. Relative paths are resolved against `$(PublishDir)`. |
| `DotNetBrowserBrandingToolPath` | Bundled tool if available; otherwise `chromium_branding.exe` on Windows or `chromium_branding` on Linux/macOS | Explicit path to the branding tool executable. |
| `DotNetBrowserBrandingToolArguments` | empty | Optional custom tool arguments. Supports `{source}`, `{destination}`, and `{params}` placeholders. If empty, the task uses the default `-p`, `-b`, and `-o` arguments. |
| `DotNetBrowserBrandingWorkingDirectory` | Prepared source path | Working directory for the branding tool process. |
| `DotNetBrowserBrandingStageAssets` | `true` | Copies relative asset paths from `branding.params.json` into the prepared binaries directory before branding. |
| `DotNetBrowserBrandingAssetsBasePath` | Directory of `DotNetBrowserBrandingParamsFile` | Base path for relative asset files referenced in `branding.params.json`. |
| `DotNetBrowserBrandingKeepTemporaryExtraction` | `false` | Keeps temporary extracted binaries after branding. Useful for diagnostics. |
| `DotNetBrowserBrandingRepackEnabled` | `false` | Packs branded binaries back into a runtime-extractable container. See [Repacking into a runtime-extractable container](#repacking-into-a-runtime-extractable-container). |
| `DotNetBrowserBrandingRepackDestinationPath` | `$(PublishDir)branded-container/` | Output path for the repacked container assembly. |
| `DotNetBrowserBrandingRepackKeepDirectoryOutput` | `true` | Set to `false` to remove the plain-directory branded output once the container has been produced successfully. |
| `DotNetBrowserBrandingRepackSignCommand` | empty | Optional command to re-sign the repacked assembly. Supports the `@@BINARY_PATH@@` placeholder. |


### Repacking into a runtime-extractable container

By default, branding outputs a plain directory of Chromium binaries. If your
application runs from a mapped network drive or UNC path, every Chromium file
in that directory has to be shipped and verified individually.

Enable repacking to pack the branded binaries back into the same compact
container format DotNetBrowser normally uses, so it can be extracted to a
local per-user directory at runtime instead:

```xml
<PropertyGroup>
  <DotNetBrowserBrandingEnabled>true</DotNetBrowserBrandingEnabled>
  <DotNetBrowserBrandingParamsFile>$(MSBuildProjectDirectory)\branding.params.json</DotNetBrowserBrandingParamsFile>
  <DotNetBrowserBrandingRepackEnabled>true</DotNetBrowserBrandingRepackEnabled>
</PropertyGroup>
```

Repacking only works when the branding source is a Chromium container
assembly (`DotNetBrowser.Chromium.<Platform>.dll`), not an already-unpacked
directory. The repacked assembly must keep the same file name as the
original, so make sure your application deploys and loads it from the
`DotNetBrowserBrandingRepackDestinationPath` output in place of the original
one.

Repacking changes the assembly's bytes, which invalidates any Authenticode
signature the original assembly carried. Set
`DotNetBrowserBrandingRepackSignCommand` (same `@@BINARY_PATH@@` placeholder
convention as `branding.params.json`'s `signCommand`) to re-sign the repacked
assembly if required.

**Important**
Do not embed a certificate password or token directly in
`DotNetBrowserBrandingRepackSignCommand`. The command text is never written to
the build log, but MSBuild records task inputs in binary logs and at
diagnostic verbosity, and the command is handed to a shell, so it is visible
in the machine's process list while it runs. Reference the certificate by
thumbprint or store instead, or have the invoked script read the secret from
an environment variable.


### Use branded binaries at application startup

Configure DotNetBrowser to use the branded output directory via
`EngineOptions.ChromiumDirectory`.

The value should point to the base branded directory. DotNetBrowser appends the
current platform subdirectory automatically.


**C#**
```csharp
string chromiumDirectory = Path.Combine(AppContext.BaseDirectory, "branded");

IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumDirectory = chromiumDirectory
}.Build());
```

**VB**
```vb
Dim chromiumDirectory As String =
    Path.Combine(AppContext.BaseDirectory, "branded")

Dim engine As IEngine = EngineFactory.Create(
    New EngineOptions.Builder() With {
        .ChromiumDirectory = chromiumDirectory
    }.Build()
)
```



For a publish output where branding writes to `publish/branded/WindowsX64`, set
`ChromiumDirectory` to `publish/branded`.

### Build and publish workflow

A typical branding workflow looks like this:

1. Add DotNetBrowser and the platform-specific Chromium package to the
   application project.
2. Add `DotNetBrowser.Branding`.
3. Create `branding.params.json`.
4. Configure `DotNetBrowserBrandingEnabled` and
   `DotNetBrowserBrandingParamsFile` in the project file.
5. Publish for the target runtime identifier.
6. Deploy the branded output directory together with the application.

Example Windows x64 publish command:

```powershell
dotnet publish -c Release -r win-x64
```

Example Linux x64 publish command:

```bash
dotnet publish -c Release -r linux-x64
```

Example macOS ARM64 publish command:

```bash
dotnet publish -c Release -r osx-arm64
```

Run each command on the same OS family as the target runtime.
