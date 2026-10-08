# <a id="DotNetBrowser_Net_UrlRequestJobExtensions"></a> Class UrlRequestJobExtensions

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

Provides extension methods for <xref href="DotNetBrowser.Net.UrlRequestJob" data-throw-if-not-resolved="false"></xref>.

```csharp
public static class UrlRequestJobExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJobExtensions](DotNetBrowser.Net.UrlRequestJobExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_UrlRequestJobExtensions_Write_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Int32_"></a> Write\(UrlRequestJob, Stream, int\)

Reads all bytes from <code class="paramref">stream</code> and writes them to the URL request job.

```csharp
public static void Write(this UrlRequestJob job, Stream stream, int bufferSize = 81920)
```

#### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

The URL request job to write the data to.

`stream` [Stream](https://learn.microsoft.com/dotnet/api/system.io.stream)

The stream to read the data from.

`bufferSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The size of the buffer used to read the stream. Must be greater than zero.

#### Remarks

The stream is read in chunks to avoid buffering the entire content in memory.
After all data is written, call <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or
<xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> to finish the request.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">job</code> or <code class="paramref">stream</code> is <code>null</code>.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

<code class="paramref">bufferSize</code> is less than or equal to zero, or greater than <xref href="System.Int32.MaxValue" data-throw-if-not-resolved="false"></xref> - 56.

### <a id="DotNetBrowser_Net_UrlRequestJobExtensions_WriteAsync_DotNetBrowser_Net_UrlRequestJob_System_IO_Stream_System_Threading_CancellationToken_System_Int32_"></a> WriteAsync\(UrlRequestJob, Stream, CancellationToken, int\)

Reads all bytes from <code class="paramref">stream</code> and writes them to the URL request job asynchronously.

```csharp
public static Task WriteAsync(this UrlRequestJob job, Stream stream, CancellationToken cancellationToken = default, int bufferSize = 81920)
```

#### Parameters

`job` [UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

The URL request job to write the data to.

`stream` [Stream](https://learn.microsoft.com/dotnet/api/system.io.stream)

The stream to read the data from.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

The token to monitor for cancellation requests.

`bufferSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The size of the buffer used to read the stream. Must be greater than zero.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

#### Remarks

<p>
    The stream is read in chunks to avoid buffering the entire content in memory.
    The calling thread is released while waiting for each chunk to be sent to the
    browser engine, making this method suitable for use inside <code>Task.Run</code> or
    <code>async</code> handlers.
</p>
<p>
    After all data is written, call <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or
    <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> to finish the request.
</p>

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">job</code> or <code class="paramref">stream</code> is <code>null</code>.

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

<code class="paramref">bufferSize</code> is less than or equal to zero, or greater than <xref href="System.Int32.MaxValue" data-throw-if-not-resolved="false"></xref> - 56.

