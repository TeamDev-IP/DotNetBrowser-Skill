# <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs"></a> Class KeyCharEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for key events which provide a character.

```csharp
public class KeyCharEventArgs : KeyEventArgs, IKeyCharEventArgs, IKeyEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md) ← 
[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyCharEventArgs.md)

#### Derived

[KeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyPressedEventArgs.md), 
[KeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyTypedEventArgs.md)

#### Implements

[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyCharEventArgs.md), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.IKeyEventArgs.md)

#### Inherited Members

[KeyEventArgs.KeyLocation](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_KeyLocation), 
[KeyEventArgs.Modifiers](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_Modifiers), 
[KeyEventArgs.VirtualKey](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_VirtualKey), 
[KeyEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_Equals\_System\_Object\_), 
[KeyEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_GetHashCode), 
[KeyEventArgs.Equals\(KeyEventArgs\)](DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md\#DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_Equals\_DotNetBrowser\_Input\_Keyboard\_Events\_KeyEventArgs\_), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_KeyChar"></a> KeyChar

Gets or sets the character associated with this event.

```csharp
public string KeyChar { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_"></a> Equals\(KeyCharEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(KeyCharEventArgs other)
```

#### Parameters

`other` [KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.KeyCharEventArgs.md)

The object to compare with the current object.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

