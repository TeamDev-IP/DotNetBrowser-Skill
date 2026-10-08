
# Deployment

**Lead**
This guide describes the ways to distribute an application built with
DotNetBrowser and what to include in the deployment package.


## What you distribute

The deployment package of a DotNetBrowser-based application consists of three
parts:

1. Your application and its own dependencies.
2. The DotNetBrowser assemblies. See [Package contents](#package-contents) for
   the complete list.
3. The Chromium runtime — the browser engine that DotNetBrowser launches as a
   separate process.

The first two parts are the same in every case. The third one is where you have
a choice, and that choice is what the distribution modes below describe.

**Note**
You do not need to install Chromium or Google Chrome on the target machine.
DotNetBrowser uses and deploys its own
[Chromium build](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/).


## Distribution modes

DotNetBrowser supplies the Chromium runtime inside the platform-specific
`DotNetBrowser.Chromium.<Platform>.dll` assemblies. Chromium cannot run from
inside a .NET assembly, so its binaries must be unpacked into a directory on
disk before the engine starts. The three distribution modes differ in when that
happens and who performs it.


| **Mode** | **Package size** | **First start** | **Internet at runtime** |
|---|---|---|---|
| [Packed Chromium runtime](#packed-chromium-runtime) | Smaller | Slower: one-time unpacking | Not required |
| [Unpacked Chromium runtime](#unpacked-chromium-runtime) | Larger | Fastest | Not required |
| [Chromium runtime over the network](#chromium-runtime-over-the-network) | Smallest | Slowest | Required |


## Packed Chromium runtime

This is the default mode. You include the
`DotNetBrowser.Chromium.<Platform>.dll` assemblies in the deployment package,
and DotNetBrowser unpacks the Chromium binaries on the target machine.

**What to include:** the assemblies listed in
[Package contents](#package-contents), including the Chromium assembly for
every platform your application supports.

**What happens at runtime:** during the first launch, DotNetBrowser checks the
Chromium binaries directory. If the required files are not there, it extracts
them from the Chromium assembly. On Windows, the default directory is
`%LocalAppData%\Temp\dotnetbrowser-chromium`. On Linux and macOS, it is the
user's temp directory. The subsequent launches reuse the extracted binaries.
See [Extraction](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#extraction) for the details.

To place the binaries elsewhere, set the [Chromium binaries
directory](docs/guides/gs/engine/#chromium-binaries-directory) through
`EngineOptions.ChromiumDirectory` or through the `DOTNETBROWSER_CHROMIUM_DIR`
environment variable.

**Requirements and trade-offs:**

- The target machine needs a writable directory for the Chromium binaries.
- Unpacking makes the first launch slower. On a machine with an i7 processor,
  16 GB of RAM, and an SSD, it takes 2–3 seconds. Antivirus software that
  checks the library binaries adds to that time. See [Slow startup on
  Windows](docs/guides/troubleshoot/common-issues/#slow-startup-on-windows).
- The deployment package is smaller than with the unpacked binaries, because
  the Chromium assemblies store the binaries in a compressed form.

Use this mode unless one of the constraints below applies to your application.

## Unpacked Chromium runtime

In this mode, you unpack the Chromium binaries during the build or publish
stage and ship the resulting directory as a part of the deployment package.
Nothing is extracted on the target machine.

To unpack the binaries during the publish stage, add the
`DotNetBrowser.Chromium.Extraction` MSBuild package to your application
project:

```xml
<ItemGroup>
  <PackageReference Include="DotNetBrowser.Chromium.Extraction"
                    Version="..."
                    PrivateAssets="all" />
</ItemGroup>

<PropertyGroup>
  <DotNetBrowserExtractionEnabled>true</DotNetBrowserExtractionEnabled>
  <DotNetBrowserExtractionDuringPublish>true</DotNetBrowserExtractionDuringPublish>
</PropertyGroup>
```

Then publish the application for the target runtime:

```powershell
dotnet publish -c Release -r win-x64
```

By default, the publish-time extraction writes the binaries to
`$(PublishDir)unpacked/` and appends a platform-specific subdirectory such as
`WindowsX64`, `LinuxArm64`, or `MacX64`. Point `ChromiumDirectory` at the base
directory, without the platform subdirectory — DotNetBrowser appends the
current one at runtime:


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



For the complete list of the extraction properties and the runtime identifier
resolution rules, see
[Pre-extracting Chromium binaries](https://teamdev.com/dotnetbrowser/docs/tutorials/chromium-extraction/). To
change the executable names, icons, or macOS bundle metadata of the unpacked
binaries, see [Branding Chromium binaries](https://teamdev.com/dotnetbrowser/docs/tutorials/chromium-branding/).

**Important**
Unpack the binaries on the same operating system family as the target runtime.
For example, unpack the Linux binaries on Linux and the macOS binaries on
macOS. This preserves the executable permissions, symbolic links, and platform
bundle structure.


**Requirements and trade-offs:**

- The deployment package is larger, because the unpacked binaries take more
  space than the compressed Chromium assemblies.
- The first launch is as fast as any subsequent one.
- DotNetBrowser extracts nothing on the target machine, because the required
  binaries are already in place.

This is the only supported mode for the applications published with Native AOT,
where assembly loading is unavailable. See
[Trimming & Native AOT](https://teamdev.com/dotnetbrowser/docs/guides/gs/aot-support/).

## Chromium runtime over the network

In this mode, the deployment package contains no Chromium assemblies at all.
The application obtains them over the network when DotNetBrowser needs them.

**Note**
Unlike the two modes above, this one is not a built-in DotNetBrowser feature.
The application implements it and hosts the service that supplies the
assemblies.


DotNetBrowser uses the standard .NET assembly loading logic to locate the
Chromium assembly, so the application can supply it through the
[AppDomain.AssemblyResolve](https://learn.microsoft.com/en-us/dotnet/api/system.appdomain.assemblyresolve)
event:

1. Register a custom handler of the `AppDomain.AssemblyResolve` event.
2. In the handler, filter out the requests for the assemblies whose names start
   with `DotNetBrowser.Chromium`.
3. Use the fully qualified assembly name to prepare a network request.
4. Perform the request and obtain the assembly as an array of bytes.
5. Load the assembly from the bytes and return it from the handler.

After that, DotNetBrowser unpacks the binaries and launches Chromium as usual.
For the reference implementation and the example projects, see [Downloading &
Installing Chromium Runtime](docs/tutorials/binaries-over-network/).

**Requirements and trade-offs:**

- The deployment package is the smallest of the three modes.
- The target machine needs access to the service that hosts the assemblies.
  Without it, the engine cannot start.
- Initialization takes longer, because it includes downloading the assembly.
- Memory usage grows during initialization, because DotNetBrowser unpacks the
  binaries from an in-memory assembly. In 32-bit environments, this can lead to
  out of memory errors.

## Choosing a mode

- For most desktop applications, use the packed Chromium runtime. It requires
  no additional configuration.
- If the cold start time matters, if the application directory is read-only, or
  if you publish with Native AOT, use the unpacked Chromium runtime.
- If the size of the installer is restricted, and the target machines can reach
  your service, supply the Chromium runtime over the network.

## Package contents

DotNetBrowser is supplied in a few dynamic libraries. Some of them are related
to DotNetBrowser itself and others to the appropriate Chromium binary files.

Here's a list of the libraries provided in DotNetBrowser distribution package:


| **Assembly** | **Size** | **References** | **Description** |
|---|---|---|---|
| DotNetBrowser.dll | ~240KB |  | Data classes and  interfaces |
| DotNetBrowser.Core.dll | ~2MB | DotNetBrowser.dll<br>DotNetBrowser.Logging.dll | Core implementation |
| DotNetBrowser.Logging.dll | ~23KB |  | DotNetBrowser Logging  API<br>implementation |
| DotNetBrowser.Chromium.Win-x86.dll | ~115MB |  | Chromium binaries for<br>Windows 32-bit |
| DotNetBrowser.Chromium.Win-x64.dll | ~120MB |  | Chromium binaries for<br>Windows 64-bit |
| DotNetBrowser.Chromium.Win-arm64.dll | ~115MB |  | Chromium binaries for<br>Windows ARM64 |
| DotNetBrowser.Chromium.Linux-x64.dll | ~125MB |  | Chromium binaries for<br>Linux 64-bit |
| DotNetBrowser.Chromium.Linux-arm64.dll | ~135MB |  | Chromium binaries for<br>Linux ARM64 |
| DotNetBrowser.Chromium.macOS-x64.dll | ~111MB |  | Chromium binaries for<br>macOS 64-bit |
| DotNetBrowser.Chromium.macOS-arm64.dll | ~115MB |  | Chromium binaries for<br>macOS ARM64 |
| DotNetBrowser.AvaloniaUi.dll | ~180KB | DotNetBrowser.dll<br>DotNetBrowser.Core.dll | Classes and interfaces for<br>embedding into an Avalonia 11 UI app |
| DotNetBrowser.AvaloniaUi.v12.dll | ~180KB | DotNetBrowser.dll<br>DotNetBrowser.Core.dll | Classes and interfaces for<br>embedding into an Avalonia 12 UI app |
| DotNetBrowser.Wpf.dll | ~170KB | DotNetBrowser.dll<br>DotNetBrowser.Core.dll | Classes and interfaces for<br>embedding into  a WPF app |
| DotNetBrowser.WinForms.dll | ~120KB | DotNetBrowser.dll<br>DotNetBrowser.Core.dll | Classes and interfaces for<br>embedding into  a WinForms<br>app |
| Google.Protobuf.dll | ~490KB |  | Protocol Buffers<br>implementation for .NET.<br>It is used to perform<br>communication between<br>the .NET side and<br>Chromium engine |


The sections below list the libraries to include for each target platform.

### Windows

**AnyCPU**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Win-x86.dll`, `DotNetBrowser.Chromium.Win-x64.dll`,
`DotNetBrowser.Chromium.Win-arm64.dll`, and `Google.Protobuf.dll`.
DotNetBrowser checks the architecture of the application and uses the matching
Chromium binaries.

**x86**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Win-x86.dll`, and `Google.Protobuf.dll`. Chromium
32-bit binaries are supported in both Windows 32-bit and 64-bit environments.

**x64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Win-x64.dll`, and `Google.Protobuf.dll`. In a 32-bit
.NET application, an exception is thrown.

**ARM64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Win-arm64.dll`, and `Google.Protobuf.dll`. These
libraries are used in the ARM64 .NET applications.

Add `DotNetBrowser.Wpf.dll`, `DotNetBrowser.WinForms.dll`,
`DotNetBrowser.AvaloniaUi.dll`, or `DotNetBrowser.AvaloniaUi.v12.dll` depending
on the framework of your .NET application.

### Linux

**x64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Linux-x64.dll`, and `Google.Protobuf.dll`. In a 32-bit
.NET application, an exception is thrown.

**ARM64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.Linux-arm64.dll`, and `Google.Protobuf.dll`. In an ARM
.NET application, an exception is thrown.

Add `DotNetBrowser.AvaloniaUi.dll` or `DotNetBrowser.AvaloniaUi.v12.dll` if your
application uses Avalonia UI.

### macOS

**x64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.macOS-x64.dll`, and `Google.Protobuf.dll`. In a 32-bit
.NET application, an exception is thrown.

**ARM64**<br>
`DotNetBrowser.dll`, `DotNetBrowser.Core.dll`, `DotNetBrowser.Logging.dll`,
`DotNetBrowser.Chromium.macOS-arm64.dll`, and `Google.Protobuf.dll`. In an ARM
.NET application, an exception is thrown.

Add `DotNetBrowser.AvaloniaUi.dll` or `DotNetBrowser.AvaloniaUi.v12.dll` if your
application uses Avalonia UI.

## Citrix

DotNetBrowser can be used in Citrix environment with Windows Server 2016 and higher.

To run Chromium and DotNetBrowser, it’s required to disable [Citrix API Hooks](https://support.citrix.com/article/CTX107825/how-to-disable-citrix-api-hooks-on-a-perapplication-basis). 

The API hooks should be disabled for `chromium.exe` file located in [Chromium binaries directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-binaries-directory).


**Note**
Alternative solution is to disable [Chromium sandbox](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox). Keep in mind that this is a security risk. Find more information about sandbox in this [article.](https://chromium.googlesource.com/chromium/src/+/master/docs/design/sandbox.md#App-Container-low-box-token)

