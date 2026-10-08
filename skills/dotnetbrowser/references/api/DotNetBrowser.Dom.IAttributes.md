# <a id="DotNetBrowser_Dom_IAttributes"></a> Interface IAttributes

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

A dictionary that contains <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> attributes. Modifying this dictionary
will lead to modifying the element attributes.

```csharp
public interface IAttributes : IAutoDisposable, IDictionary<string, string>, ICollection<KeyValuePair<string, string>>, IEnumerable<KeyValuePair<string, string>>, IEnumerable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md), 
[IDictionary<string, string\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2), 
[ICollection<KeyValuePair<string, string\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.icollection\-1), 
[IEnumerable<KeyValuePair<string, string\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

## Methods

### <a id="DotNetBrowser_Dom_IAttributes_AsReadOnly"></a> AsReadOnly\(\)

Gets a read-only dictionary that contains a snapshot of the attributes of the current element.

```csharp
IReadOnlyDictionary<string, string> AsReadOnly()
```

#### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>

The dictionary that contains a snapshot of the attributes of the current element.
The returned dictionary will be empty if the element doesn't have any attributes.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IAttributes" data-throw-if-not-resolved="false"></xref> has already been disposed.

