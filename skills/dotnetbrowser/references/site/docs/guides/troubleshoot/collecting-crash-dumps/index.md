
# Collecting crash dumps

DotNetBrowser runs Chromium in a separate native process. An error in the Chromium engine can lead to unexpected
process termination. When this happens, Chromium generates a crash dump file with the debug information.

**Note**
If Chromium process is unexpectedly terminated, and you received the 
[Engine.Disposed][engine-crashed] event with non-zero exit code, [submit a ticket][freshdesk]  and 
send us the generated crash dump file.


## Where to find crash dump files

When one of the Chromium processes crashes, DotNetBrowser generates a crash dump file. The location of the dump file
depends on the platform:

- Windows: `%appdata%\DotNetBrowser\dotnetbrowser.dmp.dir`
- Linux: `$HOME/.config/DotNetBrowser/dotnetbrowser.dmp.dir`
- macOS: `$HOME/Library/Application Support/DotNetBrowser/dotnetbrowser.dmp.dir`

To change the default directory, use the `EngineOptions.CrashDumpDirectory` property:


**C#**
```csharp
EngineOptions.CrashDumpDirectory = "C:\\DotNetBrowser\\crash-dumps";
```

**VB**
```vb
EngineOptions.CrashDumpDirectory = "C:\DotNetBrowser\crash-dumps"
```



[engine-crashed]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#engine-crashed
[freshdesk]: https://dotnetbrowser.support.teamdev.com/support/tickets/new
