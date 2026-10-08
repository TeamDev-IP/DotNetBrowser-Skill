
# Trimming and Native AOT Support in DotNetBrowser

**Lead**
This article explains what changed, what you can do with it, and how to configure your application correctly when using these deployment modes.


## Trimming

Trimming is a .NET publish-time feature that removes IL code the linker determines is never called. The result is a smaller deployment: unreferenced types, methods, and resources are stripped from the output.
The risk is that code discovered only at runtime through reflection or dynamic loading can be cut — causing `MissingMethodException` or similar failures at runtime.

To be safe for trimmed consumers, a library must declare `IsTrimmable=true` and annotate all code paths so the linker knows what to preserve.

## Native AOT

Native AOT compiles your entire .NET application to a standalone native binary at publish time.
There is no JIT compiler at runtime, no reflection-based code generation, and no `Assembly.Load`.
This dramatically reduces startup time and memory overhead — but it is the strictest deployment mode .NET supports.

## Changes in DotNetBrowser

### Compatible Packages

All core DotNetBrowser packages now declare `IsTrimmable=true` and `IsAotCompatible=true` for **.NET 8** targets:

| Package                        | Description                |
|--------------------------------|----------------------------|
| `DotNetBrowser`                | Public API surface         |
| `DotNetBrowser.Core`           | Core implementation        |
| `DotNetBrowser.Logging`        | Logging infrastructure     |
| `DotNetBrowser.AvaloniaUi`     | Avalonia 11 UI integration |
| `DotNetBrowser.AvaloniaUi.v12` | Avalonia 12 UI integration |

**Note**
**Note:** DotNetBrowser supports trimming and AOT only for console and Avalonia UI applications.


## Requirements for Native AOT Deployment

Because assembly loading is unavailable in Native AOT mode, **built-in Chromium binaries extraction is not supported**. It is necessary to deploy the Chromium binaries to a known directory before the application starts.

### Step 1 — Pre-deploy the Chromium Binaries

Copy the Chromium binaries to a directory on the target machine. The expected layout inside that directory is platform and architecture-specific:

```
<chromium-dir>/
  binaries for Windows  → WindowsX86/, WindowsX64/, WindowsArm64/
  binaries for Linux    → LinuxX64/, LinuxArm64/
  binaries for macOS    → MacX64/, MacArm64/
```

### Step 2 — Tell DotNetBrowser Where They Are

**Option A — environment variable** (no code changes required):

```bash
# Linux / macOS
export DOTNETBROWSER_CHROMIUM_DIR=/opt/myapp/chromium

# Windows
set DOTNETBROWSER_CHROMIUM_DIR=C:\myapp\chromium
```

**Option B — `EngineOptions.ChromiumDirectory`** (configured in code):


**C#**
```csharp
var engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumDirectory = "/opt/myapp/chromium"
}.Build());
```

**VB**
```vb
Dim engine = EngineFactory.Create(
    New EngineOptions.Builder() With {
        .ChromiumDirectory = "/opt/myapp/chromium"
    }.Build()
)
```



If neither option is configured and the binaries are missing, DotNetBrowser throws `ChromiumBinariesMissingException`.

## Publishing with Native AOT

Minimal `.csproj` configuration for a Native AOT application using DotNetBrowser and Avalonia UI on Linux:

```xml
<PropertyGroup>
  <OutputType>WinExe</OutputType>
  <TargetFramework>net8.0</TargetFramework>
  <PublishAot>true</PublishAot>
  <Nullable>enable</Nullable>
</PropertyGroup>

<ItemGroup>
  <PackageReference Include="DotNetBrowser.AvaloniaUi" Version="..." />
</ItemGroup>
```

Publish command:

```bash
dotnet publish -c Release -r linux-x64
```

The publish output **does not** include Chromium binaries. Deploy them separately and configure the path as described above.

## Publishing with Trimming Only

If you want smaller output without Native AOT, enable trimming alone:

```xml
<PropertyGroup>
  <OutputType>WinExe</OutputType>
  <TargetFramework>net8.0</TargetFramework>
  <PublishTrimmed>true</PublishTrimmed>
  <Nullable>enable</Nullable>
</PropertyGroup>

<ItemGroup>
  <PackageReference Include="DotNetBrowser.AvaloniaUi" Version="..." />
</ItemGroup>
```

In this mode, Chromium binaries **can** be extracted automatically from the NuGet package on first launch, the same as a normal application.
The only required deployment step is to include the `DotNetBrowser.Chromium.X.dll` assembly, as it is not automatically copied during publishing due to the absence of a direct reference.

## Supported UI Frameworks

In this release, trimming and Native AOT are supported only by the Avalonia UI integration.

**WPF, WinForms and WinUI3** are not trimming and Native AOT compatible.

## Known Limitations

**Chromium binaries must be pre-deployed in AOT mode.** There is no automatic extraction from NuGet embedded resources in Native AOT applications.

**JS reflection-based convenience overloads.** Some `IJsObject` interop helpers use reflection internally.
These paths are annotated and safe to call, but if you use `dynamic`-typed JS results heavily, verify the behavior in your specific AOT use case.

**Calling .NET from JavaScript.** It is necessary to add the `[DynamicDependency(DynamicallyAccessedMemberTypes.All, typeof(MyObject))]` attribute to ensure that the injected object is preserved during trimming.
Without this attribute, the object may be removed by the trimmer and will not be available at runtime.
Here is a code sample:


**C#**
```csharp
public class MyObject {
    [DynamicDependency(DynamicallyAccessedMemberTypes.All, typeof(MyObject))]
    public string SayHelloTo(string firstName) {
        return "Hello " + firstName + "!";
    }
}
```

**VB**
```vb
Public Class MyObject
    <DynamicDependency(DynamicallyAccessedMemberTypes.All, GetType(MyObject))>
    Public Function SayHelloTo(ByVal firstName As String) As String
        Return "Hello " & firstName & "!"
    End Function
End Class
```




**C#**
```csharp
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
window.Properties["MyObject"] = new MyObject();
```

**VB**
```vb
Dim window As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("window").Result
window.Properties("MyObject") = New MyObject()
```



After that, you can refer to the object and call its method from the JavaScript code:

```js
console.log(window.MyObject.SayHelloTo("John"));
```
