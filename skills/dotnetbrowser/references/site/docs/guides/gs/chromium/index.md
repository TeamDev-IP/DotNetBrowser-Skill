
# Chromium

**Lead**
This guide describes how to work with the Chromium build used by DotNetBrowser.


**Note**
You do not need to install Chromium or Google Chrome on the target environment to use DotNetBrowser as it uses and deploys its own Chromium build.


## Binaries

Chromium binaries for each supported platform are located inside the corresponding DotNetBrowser DLLs:

- `DotNetBrowser.Chromium.Win-x86.dll` – Chromium binaries for Windows 32-bit.
- `DotNetBrowser.Chromium.Win-x64.dll` – Chromium binaries for Windows 64-bit.
- `DotNetBrowser.Chromium.Win-arm64.dll` – Chromium binaries for Windows ARM64.
- `DotNetBrowser.Chromium.Linux-x64.dll` – Chromium binaries for Linux 64-bit.
- `DotNetBrowser.Chromium.Linux-arm64.dll` – Chromium binaries for Linux ARM64.
- `DotNetBrowser.Chromium.macOS-x64.dll` – Chromium binaries for macOS 64-bit.
- `DotNetBrowser.Chromium.macOS-arm64.dll` – Chromium binaries for macOS ARM64 (Apple Silicon).

To use Chromium, you need to extract its binaries.

### Extraction

DotNetBrowser extracts the Chromium binaries for the target platform from the corresponding DLL during the first launch.

On Windows, they are placed in the `%LocalAppData%\Temp\dotnetbrowser-chromium` directory.

On macOS and Linux, the binaries are extracted into the user’s temp directory.

DotNetBrowser checks whether the directory contains the required Chromium files. If no files are found, it extracts the binaries from the DLLs referenced in the application.

You can customize the default path to the directory, where the binaries are extracted, or extract the binaries programmatically and tell the library where they are located:


**C#**
```csharp
EngineOptions options = new EngineOptions.Builder
{
    ChromiumDirectory = @"C:\Users\Me\.DotNetBrowser"
}
.Build();
var binariesExtractor = new ChromiumBinariesExtractor();
binariesExtractor.ExtractBinariesIfNecessary(options);
// ...
engine = EngineFactory.Create(options);
```

**VB**
```vb
Dim options = New EngineOptions.Builder With 
{
    .ChromiumDirectory = "C:\Users\Me\.DotNetBrowser\chromium"
}.Build()
Dim binariesExtractor = New ChromiumBinariesExtractor()
binariesExtractor.ExtractBinariesIfNecessary(options)
' ...
engine = EngineFactory.Create(options)
```




### Chromium Version

You can obtain the information on Chromium version used by the current version of DotNetBrowser as `ChromiumInfo.Version` constant value. This field allows you to return the version of Chromium engine programmatically in your project.

### Location

You can specify the path to the Chromium binaries directory using `EngineOptions` when constructing the `IEngine` as shown in the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumDirectory = @"C:\Users\Me\.DotNetBrowser\chromium"
}
.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .ChromiumDirectory = "C:\Users\Me\.DotNetBrowser\chromium"
}.Build())
```



The path can be either relative or absolute.

**Note**

If the directory already has the required Chromium binaries, the library will not perform the extraction.
<br><br>If the directory is corrupted and some Chromium files are missing, DotNetBrowser will extract the binaries and overwrite the existing files.


Also, it is possible to set the Chromium binaries directory using the `DOTNETBROWSER_CHROMIUM_DIR` environment variable:
```bash
# Linux / macOS
export DOTNETBROWSER_CHROMIUM_DIR=/opt/myapp/chromium

# Windows
set DOTNETBROWSER_CHROMIUM_DIR=C:\myapp\chromium
```

### Verification

Each DotNetBrowser version is only compatible with its own Chromium binaries. The binaries for a specific version do not support other DotNetBrowser versions.

To make sure that the Chromium binaries are compatible with the current DotNetBrowser version, the library verifies the binaries.

## Switches

Chromium accepts the command line [switches](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-switches) that change the behavior of the features, help to debug, or turn the experimental features on.

**Note**
DotNetBrowser does not support all the Chromium switches. Therefore, we recommend configuring Chromium using the [Engine Options](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#engine-options) instead of switches.


## Sandbox

DotNetBrowser supports Chromium Sandbox on Windows, Linux, and macOS. The sandbox is enabled by default and provides
important isolation and security for Chromium subprocesses.

You can disable the sandbox using the corresponding `IEngine` option:


**C#**
```csharp
engine = EngineFactory.Create(new EngineOptions.Builder 
{
    SandboxDisabled  = true
}
.Build());
```

**VB**
```vb
engine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .SandboxDisabled = True
}.Build())
```



**Important**
Disabling the sandbox significantly reduces security. Do not disable it if your application loads untrusted HTML,
such as content from external sources or user-generated input. Doing so can expose your system to serious security risks.


### Linux

Chromium relies on [user namespaces](https://man7.org/linux/man-pages/man7/namespaces.7.html) to sandbox subprocesses.
When this feature is unavailable, DotNetBrowser cannot start Chromium and throws a `EngineInitializationException`
during `IEngine` initialization.

On Debian 10, user namespaces are disabled by default for unprivileged users. Ubuntu also supports toggling them through
a kernel parameter. On these systems, you can enable user namespaces with:

```bash
sudo sysctl -w kernel.unprivileged_userns_clone=1
echo 'kernel.unprivileged_userns_clone=1' | sudo tee -a /etc/sysctl.d/99-enable-unprivileged-userns.conf
```

On Ubuntu 23.10 and later, user namespaces are further restricted by AppArmor. To relax this restriction
configure the following parameter:

```bash
sudo sysctl -w kernel.apparmor_restrict_unprivileged_userns=0
echo 'kernel.apparmor_restrict_unprivileged_userns=0' | sudo tee -a /etc/sysctl.d/99-enable-unprivileged-userns.conf
```

Other Linux distributions enable user namespaces by default and do not require additional configuration.

If you are unable to modify the environment configuration to enable user namespaces, you can
[disable](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox) the Chromium sandbox. This approach significantly reduces security and should
only be considered as a last resort.

## Chrome extensions

DotNetBrowser does not support the extensions designed for the Chrome application.

The library integrates only with the web browser control that renders the web content. Thus, it does not have the Chrome GUI, with elements like tool bar and context menu, required to integrate the extensions.
