# <a id="DotNetBrowser_Net_FileValue"></a> Class FileValue

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class FileValue : IFileValue
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FileValue](DotNetBrowser.Net.FileValue.md)

#### Implements

[IFileValue](DotNetBrowser.Net.IFileValue.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_FileValue__ctor_System_String_DotNetBrowser_Net_MimeType_System_String_"></a> FileValue\(string, MimeType, string\)

Constructor for FileValue.

```csharp
public FileValue(string fileName, MimeType contentType, string filePath)
```

#### Parameters

`fileName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file name. Cannot be empty.

`contentType` [MimeType](DotNetBrowser.Net.MimeType.md)

A string representing the content type determined by the file extension. Equals
`application/octet-stream` when there's no MIME type associated with the file extension.

`filePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file path. Cannot be empty.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when file name or path is null or empty.

### <a id="DotNetBrowser_Net_FileValue__ctor_System_String_DotNetBrowser_Net_MimeType_System_Byte___"></a> FileValue\(string, MimeType, byte\[\]\)

Constructor for FileValue.

```csharp
public FileValue(string fileName, MimeType contentType, byte[] bytes)
```

#### Parameters

`fileName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The file name. Cannot be empty.

`contentType` [MimeType](DotNetBrowser.Net.MimeType.md)

A string representing the content type determined by the file extension. Equals
`application/octet-stream` when there's no MIME type associated with the file extension.

`bytes` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The byte sequence representing the file upload data segment.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when file name is null or empty.
when bytes array is null.

## Properties

### <a id="DotNetBrowser_Net_FileValue_Bytes"></a> Bytes

The file value as an array of bytes.

```csharp
public byte[] Bytes { get; }
```

#### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

### <a id="DotNetBrowser_Net_FileValue_ContentType"></a> ContentType

The content type determined by the file extension. Equals
<code>application/octet-stream</code> when there is no MIME type associated with the file
extension.

```csharp
public MimeType ContentType { get; }
```

#### Property Value

 [MimeType](DotNetBrowser.Net.MimeType.md)

### <a id="DotNetBrowser_Net_FileValue_FileName"></a> FileName

The file name.

```csharp
public string FileName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_FileValue_FilePath"></a> FilePath

The file value as a file path.

```csharp
public string FilePath { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

