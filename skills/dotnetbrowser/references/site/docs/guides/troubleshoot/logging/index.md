
# Logging

**Lead**
This guide describes how to configure logging for the library.


The root cause of many issues can be detected by analyzing DotNetBrowser log messages.

**Note**
By default, logging in DotNetBrowser is disabled. But if you encounter an issue or observe some unexpected behavior, we recommend you to do the following: 
1. Configure DotNetBrowser to save all log messages to a file. 
2. Reproduce the issue.
3. [Submit a ticket with](https://dotnetbrowser.support.teamdev.com/support/tickets/new) the collected log messages for further investigation.


## Levels of logging

DotNetBrowser supports the following logging levels: `All` > `Verbose` > `Information` > `Warning` > `Error` > `Critical` > `Off`. 

**Note**
The level `Off` can be used to turn off logging completely, and `All` is used to enable logging of all messages, including messages from Chromium.


You can change the logging level using the `LoggerProvider.Instance.Level` property.

For more information on levels of logging, refer to [MSDN description](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.sourcelevels?redirectedfrom=MSDN&view=netframework-4.5).


**Example: Setting Logging Level**

To save all log messages with the logging level `Verbose` and higher, use the DotNetBrowser Logging API as shown in the code sample below:


**C#**
```csharp
using DotNetBrowser.Logging;
using System.Diagnostics;
// ...
LoggerProvider.Instance.Level = SourceLevels.Verbose;
```

**VB**
```vb
Imports DotNetBrowser.Logging
Imports System.Diagnostics
' ...
LoggerProvider.Instance.Level = SourceLevels.Verbose
```




## Logging to a file

To print all log messages to a file, use the `LoggerProvider.Instance.FileLoggingEnabled` property of DotNetBrowser Logging API as shown in the code sample below:


**C#**
```csharp
using DotNetBrowser.Logging;
// ...
LoggerProvider.Instance.FileLoggingEnabled = true;
LoggerProvider.Instance.OutputFile = "C:\\log.txt";
```

**VB**
```vb
Imports DotNetBrowser.Logging
' ...
LoggerProvider.Instance.FileLoggingEnabled = True
LoggerProvider.Instance.OutputFile = "C:\log.txt"
```



In the sample above, the value of the `LoggerProvider.Instance.OutputFile` property represents an absolute or relative path to a file where the log messages are stored.

## Redirect DotNetBrowser logging

DotNetBrowser utilizes TraceSource for its logging. It is possible to redirect DotNetBrowser logs to another logger that is used in your application. For this purpose, you need to create your own class that derives from [TraceListener](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.tracelistener?view=netstandard-2.0) and performs redirection. Then, it is necessary to configure your trace listener class for TraceSource.

Below are the `TraceListener` implementations for two most popular logging frameworks: Serilog and NLog.

### Serilog


**C#**
```csharp
namespace Example
{
    public class SerilogTraceListener : TraceListener
    {
        private readonly string initializeData;
        private readonly Lazy<ILogger> logger;

        public SerilogTraceListener(string initializeData)
        {
            this.initializeData = initializeData;
            logger = new Lazy<ILogger>(() => Log.ForContext("Context", initializeData));
        }

        public override void Write(string message)
        {
            logger.Value.Information(message);
        }

        public override void WriteLine(string message)
        {
            logger.Value.Information(message);
        }
    }
}
```

**VB**
```vb
Namespace Example
	Public Class SerilogTraceListener
		Inherits TraceListener

		Private ReadOnly initializeData As String
		Private ReadOnly logger As Lazy(Of ILogger)

		Public Sub New(ByVal initializeData As String)
			Me.initializeData = initializeData
			logger = New Lazy(Of ILogger)(Function()
				Return Log.ForContext("Context", initializeData)
			End Function)
		End Sub

		Public Overrides Sub Write(ByVal message As String)
			logger.Value.Information(message)
		End Sub

		Public Overrides Sub WriteLine(ByVal message As String)
			logger.Value.Information(message)
		End Sub
	End Class
End Namespace
```



### NLog


**C#**
```csharp
using NLog;
using System.Diagnostics;
// Custom TraceListener that routes to NLog
public class NLogTraceListener : TraceListener
{
    private static readonly Logger logger = LogManager.GetLogger("TraceSource");

    public override void Write(string message)
    {
        logger.Info(message);
    }

    public override void WriteLine(string message)
    {
        logger.Info(message);
    }

    public override void TraceEvent(TraceEventCache eventCache,
                                    string source,
                                    TraceEventType eventType, int id,
                                    string message)
    {
        var logEvent = new LogEventInfo
        {
            LoggerName = source,
            Message = message,
            Level = ToLogLevel(eventType)
        };
        logger.Log(logEvent);
    }

    private LogLevel ToLogLevel(TraceEventType type)
    {
        switch (type)
        {
            case TraceEventType.Critical:
                return LogLevel.Fatal;
            case TraceEventType.Error:
                return LogLevel.Error;
            case TraceEventType.Warning:
                return LogLevel.Warn;
            case TraceEventType.Information:
                return LogLevel.Info;
            case TraceEventType.Verbose:
            case TraceEventType.Start:
            case TraceEventType.Stop:
            case TraceEventType.Suspend:
            case TraceEventType.Resume:
            case TraceEventType.Transfer:
                return LogLevel.Debug;
            default:
                return LogLevel.Info;
        }
    }
}
```

**VB**
```vb
Imports System.Diagnostics
Imports NLog

Public Class MyTraceListener
    Inherits TraceListener

    Private Shared ReadOnly logger As Logger = LogManager.GetLogger("TraceSource")

    Public Overrides Sub Write(message As String)
        logger.Info(message)
    End Sub

    Public Overrides Sub WriteLine(message As String)
        logger.Info(message)
    End Sub

    Public Overrides Sub TraceEvent(eventCache As TraceEventCache,
                                    source As String,
                                    eventType As TraceEventType,
                                    id As Integer,
                                    message As String)

        Dim logEvent As New LogEventInfo() With {
                .LoggerName = source,
                .Message = message,
                .Level = ToLogLevel(eventType)
                }

        logger.Log(logEvent)
    End Sub

    Private Function ToLogLevel(type As TraceEventType) As LogLevel
        Select Case type
            Case TraceEventType.Critical
                Return LogLevel.Fatal
            Case TraceEventType.[Error]
                Return LogLevel.[Error]
            Case TraceEventType.Warning
                Return LogLevel.Warn
            Case TraceEventType.Information
                Return LogLevel.Info
            Case TraceEventType.Verbose,
                TraceEventType.Start,
                TraceEventType.Stop,
                TraceEventType.Suspend,
                TraceEventType.Resume,
                TraceEventType.Transfer
                Return LogLevel.Debug
            Case Else
                Return LogLevel.Info
        End Select
    End Function
End Class
```



### Configuring `TraceListener` implementation

For .NET Framework, you can configure your trace listener class for TraceSource via `App.config`.

**Serilog**

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
  </startup>
  <system.diagnostics>
    <trace autoflush="true"/>
    <sources>
      <source name="Browser" switchValue="All">
        <listeners>
          <add name="SerilogTraceListener"
               type="Example.SerilogTraceListener, ExampleAssembly"
               initializeData="DotNetBrowser" />
        </listeners>
      </source>
      <source name="Process" switchValue="All">
        <listeners>
          <add name="SerilogTraceListener"
               type="Example.SerilogTraceListener, ExampleAssembly"
               initializeData="DotNetBrowser" />
        </listeners>
      </source>
      <source name="IPC" switchValue="All">
        <listeners>
          <add name="SerilogTraceListener"
               type="Example.SerilogTraceListener, ExampleAssembly"
               initializeData="DotNetBrowser" />
        </listeners>
      </source>
    </sources>
  </system.diagnostics>
</configuration> 
```

**NLog**

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
    <startup> 
        <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
    </startup>
  <system.diagnostics>
    <trace autoflush="true"/>
    <sources>
      <source name="Browser" switchValue="All">
        <listeners>
          <add name="NLogTraceListener"
               type="Example.NLogTraceListener, ExampleAssembly" />
        </listeners>
      </source>
      <source name="Process" switchValue="All">
        <listeners>
          <add name="NLogTraceListener"
               type="Example.NLogTraceListener, ExampleAssembly" />
        </listeners>
      </source>
      <source name="IPC" switchValue="All">
        <listeners>
          <add name="NLogTraceListener"
               type="Example.NLogTraceListener, ExampleAssembly" />
        </listeners>
      </source>
    </sources>
  </system.diagnostics>
</configuration>
```

The newer versions of .NET no longer support `App.config`. As an alternative, you can perform the trace listener configuration programmatically as shown below:


**C#**
```csharp
TraceSource.Initializing += (sender, e) =>
{
    string name = e.TraceSource.Name;
    if(name == "IPC" || name == "Browser" || name == "Process")
    {
        // Add a custom TraceListener that routes to NLog
        e.TraceSource.Listeners.Add(new NLogTraceListener());
    }
};
```

**VB**
```vb
AddHandler TraceSource.Initializing, Sub(sender, e)
    Dim name = e.TraceSource.Name
    If name = "IPC" OrElse name = "Browser" OrElse name = "Process" Then
        ' Add a custom TraceListener that routes to NLog
        e.TraceSource.Listeners.Add(New NLogTraceListener())
    End If
End Sub
```



You can find more information on configuring the trace listeners in the corresponding article:
[How to: Create and Initialize Trace Sources](https://learn.microsoft.com/en-us/dotnet/framework/debug-trace-profile/how-to-create-and-initialize-trace-sources)
