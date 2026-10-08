# <a id="DotNetBrowser_Net_UrlRequestJob"></a> Class UrlRequestJob

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The URL request job for the intercepted URL request, which allows you to provide the response data for
this URL request.

```csharp
public sealed class UrlRequestJob : IAutoDisposable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UrlRequestJob](DotNetBrowser.Net.UrlRequestJob.md)

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

#### Extension Methods

[UrlRequestJobExtensions.Write\(UrlRequestJob, Stream, int\)](DotNetBrowser.Net.UrlRequestJobExtensions.md\#DotNetBrowser\_Net\_UrlRequestJobExtensions\_Write\_DotNetBrowser\_Net\_UrlRequestJob\_System\_IO\_Stream\_System\_Int32\_), 
[UrlRequestJobExtensions.WriteAsync\(UrlRequestJob, Stream, CancellationToken, int\)](DotNetBrowser.Net.UrlRequestJobExtensions.md\#DotNetBrowser\_Net\_UrlRequestJobExtensions\_WriteAsync\_DotNetBrowser\_Net\_UrlRequestJob\_System\_IO\_Stream\_System\_Threading\_CancellationToken\_System\_Int32\_)

## Properties

### <a id="DotNetBrowser_Net_UrlRequestJob_IsClosed"></a> IsClosed

Indicates if the request is handled and all the data is sent.

```csharp
public bool IsClosed { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

The request is marked as handled when either <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref> or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> is called.

### <a id="DotNetBrowser_Net_UrlRequestJob_IsDisposed"></a> IsDisposed

Indicates if the object is already disposed.

```csharp
public bool IsDisposed { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_UrlRequestJob_UrlRequest"></a> UrlRequest

Gets the <xref href="DotNetBrowser.Net.UrlRequest" data-throw-if-not-resolved="false"></xref> associated with this job.

```csharp
public UrlRequest UrlRequest { get; }
```

#### Property Value

 [UrlRequest](DotNetBrowser.Net.UrlRequest.md)

## Methods

### <a id="DotNetBrowser_Net_UrlRequestJob_Complete"></a> Complete\(\)

Marks the request as completed. It can be used to indicate that all response data are already sent.

```csharp
public void Complete()
```

### <a id="DotNetBrowser_Net_UrlRequestJob_Fail"></a> Fail\(\)

Marks the request as failed. It can be used to indicate that an error occurred during writing the
response data.

```csharp
public void Fail()
```

### <a id="DotNetBrowser_Net_UrlRequestJob_Write_System_Byte___"></a> Write\(byte\[\]\)

Appends a chunk of the response data. This method may be called multiple
times to append several chunks.

```csharp
public void Write(byte[] data)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The response data bytes.

#### Remarks

When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
completed or failed.

### <a id="DotNetBrowser_Net_UrlRequestJob_Write_System_Byte___System_Int32_System_Int32_"></a> Write\(byte\[\], int, int\)

Appends a segment of the response data. This method may be called multiple
times to append several chunks.

```csharp
public void Write(byte[] data, int offset, int count)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The buffer containing the response data bytes.

`offset` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The zero-based byte offset in <code class="paramref">data</code>.

`count` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of bytes to write.

#### Remarks

When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
completed or failed.

### <a id="DotNetBrowser_Net_UrlRequestJob_WriteAsync_System_Byte___"></a> WriteAsync\(byte\[\]\)

Appends a chunk of the response data asynchronously. This method may be called multiple
times to append several chunks.

```csharp
public Task WriteAsync(byte[] data)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The response data bytes.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

#### Remarks

<p>
    Prefer this method over <xref href="DotNetBrowser.Net.UrlRequestJob.Write(System.Byte%5b%5d)" data-throw-if-not-resolved="false"></xref> when calling from an async context or a
    <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref>-based handler, as it does not block the
    calling thread while waiting for the data to be sent to the browser engine.
</p>
<p>
    When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
    or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
    completed or failed.
</p>

### <a id="DotNetBrowser_Net_UrlRequestJob_WriteAsync_System_Byte___System_Int32_System_Int32_"></a> WriteAsync\(byte\[\], int, int\)

Appends a segment of the response data asynchronously. This method may be called multiple
times to append several chunks.

```csharp
public Task WriteAsync(byte[] data, int offset, int count)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The buffer containing the response data bytes.

`offset` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The zero-based byte offset in <code class="paramref">data</code>.

`count` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of bytes to write.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> that represents the asynchronous write operation.

#### Remarks

<p>
    Prefer this method over <xref href="DotNetBrowser.Net.UrlRequestJob.Write(System.Byte%5b%5d%2cSystem.Int32%2cSystem.Int32)" data-throw-if-not-resolved="false"></xref> when calling from an async context or a
    <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref>-based handler, as it does not block the
    calling thread while waiting for the data to be sent to the browser engine.
</p>
<p>
    When all the chunks are written either the <xref href="DotNetBrowser.Net.UrlRequestJob.Complete" data-throw-if-not-resolved="false"></xref>
    or <xref href="DotNetBrowser.Net.UrlRequestJob.Fail" data-throw-if-not-resolved="false"></xref> method must be called to indicate that the request is
    completed or failed.
</p>

### <a id="DotNetBrowser_Net_UrlRequestJob_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
public event EventHandler Disposed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler)

