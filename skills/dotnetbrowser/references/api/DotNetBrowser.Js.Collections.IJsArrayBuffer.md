# <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer"></a> Interface IJsArrayBuffer

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript array buffer.

```csharp
public interface IJsArrayBuffer
```

## Remarks

An array buffer object can be passed between .NET and JavaScript as a method argument
or a return value.The object lifetime is bound to the lifetime of the frame this
object belongs to.When the owner frame is unloaded, all the JavaScript objects are
automatically disposed.

## Properties

### <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref>.

```csharp
long Count { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer_ToByteArray"></a> ToByteArray\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> to a new byte array.

```csharp
byte[] ToByteArray()
```

#### Returns

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

An array containing copy of the data in <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> has already been disposed.

