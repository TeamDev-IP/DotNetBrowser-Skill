# <a id="DotNetBrowser_Print_Events_PrintCompletedEventArgs_1"></a> Class PrintCompletedEventArgs<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Events](DotNetBrowser.Print.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Print.IPrintJob%601.PrintCompleted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class PrintCompletedEventArgs<TPrintSettings> : EventArgs where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The print settings type.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[PrintCompletedEventArgs<TPrintSettings\>](DotNetBrowser.Print.Events.PrintCompletedEventArgs\-1.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Print_Events_PrintCompletedEventArgs_1_IsCompletedSuccessfully"></a> IsCompletedSuccessfully

Indicates whether the printing is completed successfully.

```csharp
public bool IsCompletedSuccessfully { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_Events_PrintCompletedEventArgs_1_PrintJob"></a> PrintJob

Gets the print job associated with this event.

```csharp
public IPrintJob<TPrintSettings> PrintJob { get; }
```

#### Property Value

 [IPrintJob](DotNetBrowser.Print.IPrintJob\-1.md)<TPrintSettings\>

