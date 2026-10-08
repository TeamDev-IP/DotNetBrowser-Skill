
# Common issues

**Lead**
This guide describes how to troubleshoot frequently encountered issues.


## Startup failure on Windows

If DotNetBrowser does not start on Windows, make sure the environment meets
[system requirements][requirements] and no antivirus software interferes with it.

Even though we sign DotNetBrowser executable files with an
[extended validation][ev-certificate] signature, antivirus software may still block the applications that are not
in the whitelist.

If whitelisting DotNetBrowser doesn't help, please enable [logging][logging], reproduce the issue, collect
[crash dump files][crash-dumps], and [report the issue][freshdesk] to us.

## Video does not play

A video will not work if DotNetBrowser doesn't support the format of the video. Check the list
of [supported video and audio formats][codecs].

To play DRM-encoded content, make sure to enable [Widevine component][widevine].

## Cannot sign in to Google account

An attempt to sign in to Google Account may lead to the following message:

![Sign in Error](https://teamdev.com/dotnetbrowser/img/articles/troubleshooting/google-account-sign-in-error.webp)

We're aware of two factors that influence that:

* The [remote debugging][remote-debugging] is enabled. Google may block a login attempt if the browser
  exposes the remote debugging port.
* An outdated browser version. Consider upgrading to the latest DotNetBrowser 4.3.3.

## User data is not stored

DotNetBrowser stores cookies, cache, history, and other kinds of data in the [user data directory][user-data-dir].

By default, DotNetBrowser creates this directory when the `IEngine` starts and removes it when the engine is closed. As
a result, the login session, passwords, credit cards, and other data get deleted.

To retain the data, configure the permanent location for the user data directory:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser"
}.Build())
```



## Incorrect color profile

In certain environments, you may notice the colors displayed incorrectly. For example, the rendered content can appear 
in a yellow tone:

![Yellow background](https://teamdev.com/dotnetbrowser/img/articles/troubleshooting/yellow_background.webp)

That is caused by a non-sRGB display color profile. There are two possible solutions:

1. Set the display color profile to sRGB.
2. Force Chromium color profile by specifying the `--force-color-profile=srgb` command
   line [switch][switches].

## Slow startup on Windows

The startup time depends on the environment, the hardware performance, and the installed antivirus software.

The DotNetBrowser startup process consists of several steps. First, it extracts the necessary Chromium binaries
from DLL files. Then it launches the [Chromium main process][architecture] and sets up the connection between 
the .NET and Chromium.

Normally, the extraction of the Chromium binaries occurs only once in the environment. This step may noticeably slow
down the startup. For example, it takes 2–3 seconds on the i7/16GB RAM/512GB SSD machine. Learn how to skip
this step [here][chromium-location].

Antivirus software may check library binaries before allowing DotNetBrowser to launch them. This negatively affects the
startup time. Please try disabling the antivirus and see if it helps.

If it does not help, enable [logging][logging], reproduce the issue, and [submit a ticket][freshdesk] with 
the collected log messages and the details about your hardware.

## Unresponsive application

If your .NET application freezes, and you believe it happens because of DotNetBrowser, do the following:

1. Enable [logging][logging].
2. Reproduce the issue.
3. While the application is frozen, create a process dump.

   You can create the dump of the .NET process using such tools as [Visual Studio Debugger][visual-studio-dump], 
   [ProcDump][proc-dump], [DebugDiag][debug-diag-dump], and others.
4. Submit a [ticket][freshdesk] with the logs and the process dump file.

## Chromium process crash

DotNetBrowser runs Chromium in a separate native process. An error in this process may lead to unexpected process
termination. When this happens, the library generates one or multiple [crash dump files][crash-dumps].
These files are essential for understanding the cause of the crash.

If Chromium process is unexpectedly terminated, and you received the `Engine.Disposed` with non-zero exit code,
please [report][freshdesk] the issue and attach the generated crash dump file/files.

## Running as admin on Windows

Starting with DotNetBrowser 2.27.15 and 3.3.1 (Chromium 138), the Chromium process doesn't start when launched
with admin permissions on Windows. That is expected behavior.

Use the `--do-not-de-elevate` switch if you need to run your application with administrator
privileges:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumSwitches = { "--do-not-de-elevate" }
}.Build());
```

**VB**
```vb
Dim builder = New EngineOptions.Builder()
builder.ChromiumSwitches.Add("--do-not-de-elevate")

Dim engine As IEngine = EngineFactory.Create(builder.Build())
```



[crash-dumps]: https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/collecting-crash-dumps/
[freshdesk]: https://dotnetbrowser.support.teamdev.com/support/tickets/new
[logging]: https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/logging/
[requirements]: https://teamdev.com/dotnetbrowser/docs/guides/requirements/
[ev-certificate]: https://en.wikipedia.org/wiki/Extended_Validation_Certificate
[codecs]: https://teamdev.com/dotnetbrowser/docs/guides/gs/media/#codecs
[widevine]: https://teamdev.com/dotnetbrowser/docs/guides/gs/media/#widevine
[remote-debugging]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#remote-debugging-port
[user-data-dir]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory
[switches]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-switches
[architecture]: https://teamdev.com/dotnetbrowser/docs/guides/architecture/
[chromium-location]: https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#location
[visual-studio-dump]: https://learn.microsoft.com/en-us/visualstudio/debugger/using-dump-files?view=vs-2019#BKMK_Create_a_dump_file
[proc-dump]: https://learn.microsoft.com/en-us/sysinternals/downloads/procdump
[debug-diag-dump]: https://www.microsoft.com/en-us/download/details.aspx?id=49924
