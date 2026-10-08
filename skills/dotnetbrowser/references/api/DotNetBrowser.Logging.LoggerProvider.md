# <a id="DotNetBrowser_Logging_LoggerProvider"></a> Class LoggerProvider

Namespace: [DotNetBrowser.Logging](DotNetBrowser.Logging.md)  
Assembly: DotNetBrowser.Core.dll  

Provides access to different DotNetBrowser Loggers which are used to log Browser,
IPC and Chromium process messages.

```csharp
public class LoggerProvider : IDisposable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[LoggerProvider](DotNetBrowser.Logging.LoggerProvider.md)

#### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Logging_LoggerProvider_ChromiumLogFile"></a> ChromiumLogFile

The absolute or relative path to store Chromium log file.

```csharp
public string ChromiumLogFile { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Logging_LoggerProvider_ConsoleLoggingEnabled"></a> ConsoleLoggingEnabled

Gets or sets a value indicating whether console logging is enabled.

```csharp
public bool ConsoleLoggingEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Logging_LoggerProvider_FileLoggingEnabled"></a> FileLoggingEnabled

Gets or sets a value indicating whether file logging is enabled.

```csharp
public bool FileLoggingEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Logging_LoggerProvider_Instance"></a> Instance

The LoggerProvider instance that can be used to configure DotNetBrowser logging.

```csharp
public static LoggerProvider Instance { get; }
```

#### Property Value

 [LoggerProvider](DotNetBrowser.Logging.LoggerProvider.md)

### <a id="DotNetBrowser_Logging_LoggerProvider_Level"></a> Level

The minimal logging level of the messages that will appear in the logs.
This value will be used to filter out log messages with lower logging level.

```csharp
public SourceLevels Level { get; set; }
```

#### Property Value

 [SourceLevels](https://learn.microsoft.com/dotnet/api/system.diagnostics.sourcelevels)

### <a id="DotNetBrowser_Logging_LoggerProvider_OutputFile"></a> OutputFile

Gets or sets output file.

```csharp
public string OutputFile { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Logging_LoggerProvider_Dispose"></a> Dispose\(\)

Dispose object and  managed resources.

```csharp
public void Dispose()
```

### <a id="DotNetBrowser_Logging_LoggerProvider_Dispose_System_Boolean_"></a> Dispose\(bool\)

Dispose object and managed resources.

```csharp
protected virtual void Dispose(bool disposing)
```

#### Parameters

`disposing` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

True if managed resources should be disposed

### <a id="DotNetBrowser_Logging_LoggerProvider_Finalize"></a> \~LoggerProvider\(\)

Destructor

```csharp
protected ~LoggerProvider()
```

