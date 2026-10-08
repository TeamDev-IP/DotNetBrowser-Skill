# <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs"></a> Class KeyEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public class KeyEventArgs : IKeyEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md)

#### Derived

[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyCharEventArgs.md), 
[KeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyReleasedEventArgs.md)

#### Implements

[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyEventArgs.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation"></a> KeyLocation

Gets or sets the key location on the keyboard.

```csharp
public KeyLocation KeyLocation { get; set; }
```

#### Property Value

 [KeyLocation](DotNetBrowser.Input.Keyboard.Events.KeyLocation.md)

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers"></a> Modifiers

Gets or sets the key modifiers.

```csharp
public IKeyModifiers Modifiers { get; set; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey"></a> VirtualKey

Gets or sets the virtual key code.

```csharp
public KeyCode VirtualKey { get; set; }
```

#### Property Value

 [KeyCode](DotNetBrowser.Input.Keyboard.Events.KeyCode.md)

## Methods

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_"></a> Equals\(KeyEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(KeyEventArgs other)
```

#### Parameters

`other` [KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md)

The object to compare with the current object.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

