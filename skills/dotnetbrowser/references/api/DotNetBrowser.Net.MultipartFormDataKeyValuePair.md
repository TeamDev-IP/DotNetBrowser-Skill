# <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair"></a> Class MultipartFormDataKeyValuePair

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

A key-value pair that represents a segment of a multi-part form data. Can contain values
corresponding a form field content, an upload file content, etc.

```csharp
public sealed class MultipartFormDataKeyValuePair
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MultipartFormDataKeyValuePair](DotNetBrowser.Net.MultipartFormDataKeyValuePair.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair__ctor_System_String_DotNetBrowser_Net_FileValue_"></a> MultipartFormDataKeyValuePair\(string, FileValue\)

Creates an instance from the given key and value.

```csharp
public MultipartFormDataKeyValuePair(string key, FileValue value)
```

#### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

The form content segment key.

`value` [FileValue](DotNetBrowser.Net.FileValue.md)

The segment value representing the file content.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">key</code> is null or empty. /&gt; is null.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">value</code> is null.

### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair__ctor_System_String_System_String_"></a> MultipartFormDataKeyValuePair\(string, string\)

Creates an instance from the given key and value.

```csharp
public MultipartFormDataKeyValuePair(string key, string value)
```

#### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

The form content segment key.

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)

The segment value representing the form content segment value. Can be empty if the
<code class="paramref">key</code>does not correspond to any value. For example, an empty
form field

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">key</code> is null or empty. /&gt; is null.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">value</code> is null.

## Properties

### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_FileValue"></a> FileValue

The file representation of the data.

```csharp
public IFileValue FileValue { get; }
```

#### Property Value

 [IFileValue](DotNetBrowser.Net.IFileValue.md)

### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_Key"></a> Key

The form content segment key.

```csharp
public string Key { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_MultipartFormDataKeyValuePair_StringValue"></a> StringValue

The string representation of the data.

```csharp
public string StringValue { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

