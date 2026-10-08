# <a id="DotNetBrowser_Net_FormData"></a> Class FormData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The list of key-value pairs each representing a segment of a form data.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class FormData : UploadData, IUploadData<IReadOnlyCollection<KeyValuePair<string, string>>>, IUploadData
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.UploadData.md) ← 
[FormData](DotNetBrowser.Net.FormData.md)

#### Implements

[IUploadData<IReadOnlyCollection<KeyValuePair<string, string\>\>\>](DotNetBrowser.Net.IUploadData\-1.md), 
[IUploadData](DotNetBrowser.Net.IUploadData.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_FormData__ctor_System_Collections_Generic_IReadOnlyCollection_System_Collections_Generic_KeyValuePair_System_String_System_String___"></a> FormData\(IReadOnlyCollection<KeyValuePair<string, string\>\>\)

Creates a new instance containing the specified key-value pairs.

```csharp
public FormData(IReadOnlyCollection<KeyValuePair<string, string>> data)
```

#### Parameters

`data` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[KeyValuePair](https://learn.microsoft.com/dotnet/api/system.collections.generic.keyvaluepair\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>\>

The key-value pairs that represent segments of the form data.

## Properties

### <a id="DotNetBrowser_Net_FormData_Data"></a> Data

The key-value pairs that represent segments of the form data.

```csharp
public IReadOnlyCollection<KeyValuePair<string, string>> Data { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[KeyValuePair](https://learn.microsoft.com/dotnet/api/system.collections.generic.keyvaluepair\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>\>

