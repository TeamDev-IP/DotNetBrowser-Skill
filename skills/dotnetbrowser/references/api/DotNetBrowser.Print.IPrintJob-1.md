# <a id="DotNetBrowser_Print_IPrintJob_1"></a> Interface IPrintJob<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A printing operation that is currently in-progress.

```csharp
public interface IPrintJob<TPrintSettings> : IAutoDisposable where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The type of print settings that can be applied to this job.

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Print_IPrintJob_1_Settings"></a> Settings

Gets the configurable settings of this print job.

```csharp
TPrintSettings Settings { get; }
```

#### Property Value

 TPrintSettings

### <a id="DotNetBrowser_Print_IPrintJob_1_PageCountUpdated"></a> PageCountUpdated

Occurs when the total number of pages to be printed is updated.

```csharp
event EventHandler<PageCountUpdatedEventArgs<TPrintSettings>> PageCountUpdated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PageCountUpdatedEventArgs](DotNetBrowser.Print.Events.PageCountUpdatedEventArgs\-1.md)<TPrintSettings\>\>

#### Remarks

The page count is updated each time when the
<xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method is called.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Print_IPrintJob_1_PrintCompleted"></a> PrintCompleted

Occurs when the printing operation is completed.

```csharp
event EventHandler<PrintCompletedEventArgs<TPrintSettings>> PrintCompleted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintCompletedEventArgs](DotNetBrowser.Print.Events.PrintCompletedEventArgs\-1.md)<TPrintSettings\>\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

