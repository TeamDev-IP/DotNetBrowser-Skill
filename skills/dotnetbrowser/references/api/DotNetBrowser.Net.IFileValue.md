# <a id="DotNetBrowser_Net_IFileValue"></a> Interface IFileValue

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

File data.

```csharp
public interface IFileValue
```

## Remarks

<p>
    Depending on how the request was constructed can contain the path to a file, or the
    bytes representing a file.
</p>
<p>
    For example, it contains the path when the value is taken from an
    <code> &lt;input type="file"&gt; </code>
    element of the submitted form.
</p>
<p>
    May contain bytes in case the request in the <code>multipart/form-data</code>
    format was constructed manually in a JavaScript code.
</p>

## Properties

### <a id="DotNetBrowser_Net_IFileValue_Bytes"></a> Bytes

The file value as an array of bytes.

```csharp
byte[] Bytes { get; }
```

#### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

### <a id="DotNetBrowser_Net_IFileValue_ContentType"></a> ContentType

The content type determined by the file extension. Equals
<code>application/octet-stream</code> when there is no MIME type associated with the file
extension.

```csharp
MimeType ContentType { get; }
```

#### Property Value

 [MimeType](DotNetBrowser.Net.MimeType.md)

### <a id="DotNetBrowser_Net_IFileValue_FileName"></a> FileName

The file name.

```csharp
string FileName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_IFileValue_FilePath"></a> FilePath

The file value as a file path.

```csharp
string FilePath { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

