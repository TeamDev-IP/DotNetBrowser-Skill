# <a id="DotNetBrowser_Input_Keyboard_Events"></a> Namespace DotNetBrowser.Input.Keyboard.Events

### Classes

 [KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs)

The event arguments for key events which provide a character.

 [KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs)

 [KeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyModifiers)

 [KeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyPressedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyPressed" data-throw-if-not-resolved="false"></xref> event.

 [KeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyReleasedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyReleased" data-throw-if-not-resolved="false"></xref> event.

 [KeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyTypedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyTyped" data-throw-if-not-resolved="false"></xref> event.

### Interfaces

 [IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs)

The event arguments for key events which provide a character.

 [IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

The base interface of all event arguments for the key events.

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

The keyboard modifiers applied.

 [IKeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyPressedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyPressed" data-throw-if-not-resolved="false"></xref> event.

 [IKeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyReleasedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyReleased" data-throw-if-not-resolved="false"></xref> event.

 [IKeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyTypedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyTyped" data-throw-if-not-resolved="false"></xref> event.

### Enums

 [KeyCode](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCode)

The virtual key codes.

 [KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyLocation)

The key location on the keyboard.

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs"></a> Class KeyCharEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for key events which provide a character.

```csharp
public class KeyCharEventArgs : KeyEventArgs, IKeyCharEventArgs, IKeyEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs) ← 
[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs)

##### Derived

[KeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyPressedEventArgs), 
[KeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyTypedEventArgs)

##### Implements

[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

##### Inherited Members

[KeyEventArgs.KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation), 
[KeyEventArgs.Modifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers), 
[KeyEventArgs.VirtualKey](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey), 
[KeyEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_), 
[KeyEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode), 
[KeyEventArgs.Equals\(KeyEventArgs\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_KeyChar"></a> KeyChar

Gets or sets the character associated with this event.

```csharp
public string KeyChar { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_"></a> Equals\(KeyCharEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(KeyCharEventArgs other)
```

##### Parameters

`other` [KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs)

The object to compare with the current object.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs"></a> Class KeyEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public class KeyEventArgs : IKeyEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs)

##### Derived

[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs), 
[KeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyReleasedEventArgs)

##### Implements

[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation"></a> KeyLocation

Gets or sets the key location on the keyboard.

```csharp
public KeyLocation KeyLocation { get; set; }
```

##### Property Value

 [KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyLocation)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers"></a> Modifiers

Gets or sets the key modifiers.

```csharp
public IKeyModifiers Modifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey"></a> VirtualKey

Gets or sets the virtual key code.

```csharp
public KeyCode VirtualKey { get; set; }
```

##### Property Value

 [KeyCode](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCode)

### Methods

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_"></a> Equals\(KeyEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(KeyEventArgs other)
```

##### Parameters

`other` [KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs)

The object to compare with the current object.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers"></a> Class KeyModifiers

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class KeyModifiers : IKeyModifiers
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyModifiers)

##### Implements

[IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_AltDown"></a> AltDown

Indicates whether the Alt key is pressed.

```csharp
public bool AltDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_AltGraphDown"></a> AltGraphDown

Indicates whether the Alt Graph/Right Alt key is pressed.

```csharp
public bool AltGraphDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_ControlDown"></a> ControlDown

Indicates whether the Ctrl key is pressed.

```csharp
public bool ControlDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_MetaDown"></a> MetaDown

Indicates whether the Meta key is pressed.

```csharp
public bool MetaDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_ShiftDown"></a> ShiftDown

Indicates whether the Shift key is pressed.

```csharp
public bool ShiftDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### Methods

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_KeyModifiers_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyPressedEventArgs"></a> Class KeyPressedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyPressed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class KeyPressedEventArgs : KeyCharEventArgs, IKeyPressedEventArgs, IKeyCharEventArgs, IKeyEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs) ← 
[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs) ← 
[KeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyPressedEventArgs)

##### Implements

[IKeyPressedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyPressedEventArgs), 
[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

##### Inherited Members

[KeyCharEventArgs.KeyChar](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_KeyChar), 
[KeyCharEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_System_Object_), 
[KeyCharEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_GetHashCode), 
[KeyEventArgs.KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation), 
[KeyEventArgs.Modifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers), 
[KeyEventArgs.VirtualKey](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey), 
[KeyEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_), 
[KeyEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyReleasedEventArgs"></a> Class KeyReleasedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyReleased" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class KeyReleasedEventArgs : KeyEventArgs, IKeyReleasedEventArgs, IKeyEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs) ← 
[KeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyReleasedEventArgs)

##### Implements

[IKeyReleasedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyReleasedEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

##### Inherited Members

[KeyEventArgs.KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation), 
[KeyEventArgs.Modifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers), 
[KeyEventArgs.VirtualKey](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey), 
[KeyEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_), 
[KeyEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyTypedEventArgs"></a> Class KeyTypedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyTyped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class KeyTypedEventArgs : KeyCharEventArgs, IKeyTypedEventArgs, IKeyCharEventArgs, IKeyEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[KeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs) ← 
[KeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs) ← 
[KeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyTypedEventArgs)

##### Implements

[IKeyTypedEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyTypedEventArgs), 
[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

##### Inherited Members

[KeyCharEventArgs.KeyChar](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_KeyChar), 
[KeyCharEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_Equals_System_Object_), 
[KeyCharEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCharEventArgs_GetHashCode), 
[KeyEventArgs.KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_KeyLocation), 
[KeyEventArgs.Modifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Modifiers), 
[KeyEventArgs.VirtualKey](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_VirtualKey), 
[KeyEventArgs.Equals\(object\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_Equals_System_Object_), 
[KeyEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs"></a> Interface IKeyCharEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for key events which provide a character.

```csharp
public interface IKeyCharEventArgs : IKeyEventArgs
```

##### Implements

[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs_KeyChar"></a> KeyChar

Gets the character associated with this event.

```csharp
string KeyChar { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs"></a> Interface IKeyEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The base interface of all event arguments for the key events.

```csharp
public interface IKeyEventArgs
```

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_KeyLocation"></a> KeyLocation

Gets the key location on the keyboard.

```csharp
KeyLocation KeyLocation { get; }
```

##### Property Value

 [KeyLocation](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyLocation)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_Modifiers"></a> Modifiers

Gets the key modifiers.

```csharp
IKeyModifiers Modifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs_VirtualKey"></a> VirtualKey

Gets the virtual key code.

```csharp
KeyCode VirtualKey { get; }
```

##### Property Value

 [KeyCode](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_KeyCode)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers"></a> Interface IKeyModifiers

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The keyboard modifiers applied.

```csharp
public interface IKeyModifiers
```

### Properties

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers_AltDown"></a> AltDown

Indicates whether the Alt key is pressed.

```csharp
bool AltDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers_AltGraphDown"></a> AltGraphDown

Indicates whether the Alt Graph/Right Alt key is pressed.

```csharp
bool AltGraphDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers_ControlDown"></a> ControlDown

Indicates whether the Ctrl key is pressed.

```csharp
bool ControlDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers_MetaDown"></a> MetaDown

Indicates whether the Meta key is pressed.

```csharp
bool MetaDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Keyboard_Events_IKeyModifiers_ShiftDown"></a> ShiftDown

Indicates whether the Shift key is pressed.

```csharp
bool ShiftDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyPressedEventArgs"></a> Interface IKeyPressedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyPressed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IKeyPressedEventArgs : IKeyCharEventArgs, IKeyEventArgs
```

##### Implements

[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyReleasedEventArgs"></a> Interface IKeyReleasedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyReleased" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IKeyReleasedEventArgs : IKeyEventArgs
```

##### Implements

[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

## <a id="DotNetBrowser_Input_Keyboard_Events_IKeyTypedEventArgs"></a> Interface IKeyTypedEventArgs

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard.KeyTyped" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IKeyTypedEventArgs : IKeyCharEventArgs, IKeyEventArgs
```

##### Implements

[IKeyCharEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyCharEventArgs), 
[IKeyEventArgs](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyEventArgs)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyCode"></a> Enum KeyCode

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The virtual key codes.

```csharp
public enum KeyCode
```

### Fields

`Accept = 30` 

IME accept.



`Add = 107` 

The add key.



`Apps = 93` 

Applications key (Natural keyboard).



`Attn = 246` 

The Attn key.



`Back = 8` 

The BACKSPACE key (VK_BACK).



`BrowserBack = 166` 

The Browser Back  key.



`BrowserFavorites = 171` 

The Browser Favorites key.



`BrowserForward = 167` 

The Browser Forward key.



`BrowserHome = 172` 

The Browser Start and Home  key.



`BrowserRefresh = 168` 

The Browser Refresh key.



`BrowserSearch = 170` 

The Browser Search key.



`BrowserStop = 169` 

The Browser Stop key.



`Cancel = 3` 

Control-break processing (VK_CANCEL).



`Capital = 20` 

The CAPS LOCK key (VK_CAPITAL).



`Clear = 12` 

The CLEAR key (VK_CLEAR).



`Command = 157` 

The Command key.



`Control = 17` 

The CTRL key (VK_CONTROL).



`Convert = 28` 

IME convert.



`Crsel = 247` 

The CrSel key.



`DbeAlphanumeric = 240` 

The DBE_ALPHANUMERIC key.



`Decimal = 110` 

The decimal key.



`Delete = 46` 

The DEL key (VK_DELETE).



`Divide = 111` 

The divide key.



`Down = 40` 

The DOWN ARROW key.



`End = 35` 

The END key.



`Ereof = 249` 

The Erase EOF key.



`Escape = 27` 

ESC key.



`Execute = 43` 

The EXECUTE key



`Exsel = 248` 

The ExSel key.



`F1 = 112` 

The 'F1' key.



`F10 = 121` 

The 'F10' key.



`F11 = 122` 

The 'F11' key.



`F12 = 123` 

The 'F12' key.



`F13 = 124` 

The 'F13' key.



`F14 = 125` 

The 'F14' key.



`F15 = 126` 

The 'F15' key.



`F16 = 127` 

The 'F16' key.



`F17 = 128` 

The 'F17' key.



`F18 = 129` 

The 'F18' key.



`F19 = 130` 

The 'F19' key.



`F2 = 113` 

The 'F2' key.



`F20 = 131` 

The 'F20' key.



`F21 = 132` 

The 'F21' key.



`F22 = 133` 

The 'F22' key.



`F23 = 134` 

The 'F23' key.



`F24 = 135` 

The 'F24' key.



`F3 = 114` 

The 'F3' key.



`F4 = 115` 

The 'F4' key.



`F5 = 116` 

The 'F5' key.



`F6 = 117` 

The 'F6' key.



`F7 = 118` 

The 'F7' key.



`F8 = 119` 

The 'F8' key.



`F9 = 120` 

The 'F9' key.



`Final = 24` 

IME final mode.



`Hanguel = 21` 

IME Hanguel mode (maintained for compatibility; use <xref href="DotNetBrowser.Input.Keyboard.Events.KeyCode.Hangul" data-throw-if-not-resolved="false"></xref>).



`Hangul = 21` 

IME Hangul mode.



`Hanja = 25` 

IME Hanja mode.



`Help = 47` 

The HELP key (VK_HELP).



`Home = 36` 

The HOME key.



`Insert = 45` 

The INS key (VK_INSERT).



`Junja = 23` 

IME Junja mode.



`Kana = 21` 

IME Kana mode (VK_KANA).



`Kanji = 25` 

IME Kanji mode.



`LButton = 1` 

The left mouse button (VK_LBUTTON).



`LCmd = 91` 

The Command key.



`LControl = 162` 

The Left CONTROL key.



`LMenu = 164` 

The Left MENU  key.



`LShift = 160` 

The Left SHIFT key.



`LWin = 91` 

Left Windows key (Natural keyboard).



`LaunchApp1 = 182` 

The Start Application 1 key.



`LaunchApp2 = 183` 

The Start Application 2 key.



`LaunchMail = 180` 

The Start Mail key.



`LaunchMediaSelect = 181` 

The Select Media key.



`Left = 37` 

The LEFT ARROW key.



`MButton = 4` 

The middle mouse button (three-button mouse)



`MediaNextTrack = 176` 

The Next Track key.



`MediaPlayPause = 179` 

The Play/Pause Media key.



`MediaPrevTrack = 177` 

The Previous Track key.



`MediaStop = 178` 

The Stop Media key.



`Menu = 18` 

The ALT key (VK_MENU).



`ModeChange = 31` 

IME mode change request.



`Multiply = 106` 

The multiply key.



`Next = 34` 

The PAGE DOWN key.



`NoName = 252` 

Reserved.



`NonConvert = 29` 

IME nonconvert.



`Numlock = 144` 

The NUM LOCK key.



`Numpad0 = 96` 

The numeric keypad '0' key.



`Numpad1 = 97` 

The numeric keypad '1' key.



`Numpad2 = 98` 

The numeric keypad '2' key.



`Numpad3 = 99` 

The numeric keypad '3' key.



`Numpad4 = 100` 

The numeric keypad '4' key.



`Numpad5 = 101` 

The numeric keypad '5' key.



`Numpad6 = 102` 

The numeric keypad '6' key.



`Numpad7 = 103` 

The numeric keypad '7' key.



`Numpad8 = 104` 

The numeric keypad '8' key.



`Numpad9 = 105` 

The numeric keypad '9' key.



`Oem1 = 186` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the ';:' key.



`Oem102 = 226` 

Either the angle bracket key or the backslash key on the RT 102-key keyboard.



`Oem2 = 191` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the '/?' key.



`Oem3 = 192` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the '`~' key.



`Oem4 = 219` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the '[{' key.



`Oem5 = 220` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the '\|' key.



`Oem6 = 221` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the ']}' key.



`Oem7 = 222` 

Used for miscellaneous characters; it can vary by keyboard.
For the US standard keyboard, the 'single-quote/double-quote' key.



`Oem8 = 223` 

Used for miscellaneous characters; it can vary by keyboard.



`OemClear = 254` 

The Clear key.



`OemComma = 188` 

For any country/region, the ',' key.



`OemMinus = 189` 

For any country/region, the '-' key.



`OemPeriod = 190` 

For any country/region, the '.' key.



`OemPlus = 187` 

For any country/region, the '+' key.



`Pa1 = 253` 

The PA1 key.



`Packet = 231` 

Used to pass Unicode characters as if they were keystrokes.
The VK_PACKET key is the low word of a 32-bit Virtual Key value used for non-keyboard input methods.



`Pause = 19` 

The PAUSE key (VK_PAUSE).



`Play = 250` 

The Play key.



`Print = 42` 

The PRINT key.



`Prior = 33` 

The PAGE UP key.



`Processkey = 229` 

The IME PROCESS key.



`RButton = 2` 

The right mouse button (VK_RBUTTON).



`RCmd = 92` 

The Right Command key.



`RControl = 163` 

The Right CONTROL key.



`RMenu = 165` 

The Right MENU key.



`RShift = 161` 

The Right SHIFT key.



`RWin = 92` 

Right Windows key (Natural keyboard).



`Return = 13` 

The ENTER key (VK_RETURN).



`Right = 39` 

The RIGHT ARROW key.



`Scroll = 145` 

The SCROLL LOCK key.



`Select = 41` 

The SELECT key.



`Separator = 108` 

The separator key.



`Shift = 16` 

The SHIFT key (VK_SHIFT).



`Sleep = 95` 

Computer Sleep key.



`Snapshot = 44` 

The PRINT SCREEN / SysRq key (VK_SNAPSHOT).



`Space = 32` 

The spacebar (VK_SPACE).



`Subtract = 109` 

The subtract key.



`Tab = 9` 

The TAB key (VK_TAB).



`Unknown = 0` 

Reserved value.



`Up = 38` 

The UP ARROW key.



`Vk0 = 48` 

The '0' key.



`Vk1 = 49` 

The '1' key.



`Vk2 = 50` 

The '2' key.



`Vk3 = 51` 

The '3' key.



`Vk4 = 52` 

The '4' key.



`Vk5 = 53` 

The '5' key.



`Vk6 = 54` 

The '6' key.



`Vk7 = 55` 

The '7' key.



`Vk8 = 56` 

The '8' key.



`Vk9 = 57` 

The '9' key.



`VkA = 65` 

The 'A' key.



`VkB = 66` 

The 'B' key.



`VkC = 67` 

The 'C' key.



`VkD = 68` 

The 'D' key.



`VkE = 69` 

The 'E' key.



`VkF = 70` 

The 'F' key.



`VkG = 71` 

The 'G' key.



`VkH = 72` 

The 'H' key.



`VkI = 73` 

The 'I' key.



`VkJ = 74` 

The 'J' key.



`VkK = 75` 

The 'K' key.



`VkL = 76` 

The 'L' key.



`VkM = 77` 

The 'M' key.



`VkN = 78` 

The 'N' key.



`VkO = 79` 

The 'O' key.



`VkP = 80` 

The 'P' key.



`VkQ = 81` 

The 'Q' key.



`VkR = 82` 

The 'R' key.



`VkS = 83` 

The 'S' key.



`VkT = 84` 

The 'T' key.



`VkU = 85` 

The 'U' key.



`VkV = 86` 

The 'V' key.



`VkW = 87` 

The 'W' key.



`VkX = 88` 

The 'X' key.



`VkY = 89` 

The 'Y' key.



`VkZ = 90` 

The 'Z' key.



`VolumeDown = 174` 

The Volume Down key.



`VolumeMute = 173` 

The Volume Mute key.



`VolumeUp = 175` 

The Volume Up key.



`XButton1 = 5` 

The X1 mouse button (VK_XBUTTON1).



`XButton2 = 6` 

The X2 mouse button(VK_XBUTTON2).



`Zoom = 251` 

The Zoom key.



### See Also

[https://docs.microsoft.com/en\-us/windows/win32/inputdev/virtual\-key\-codes](https://docs.microsoft.com/en\-us/windows/win32/inputdev/virtual\-key\-codes)

## <a id="DotNetBrowser_Input_Keyboard_Events_KeyLocation"></a> Enum KeyLocation

Namespace: [DotNetBrowser.Input.Keyboard.Events](DotNetBrowser.Input.Keyboard.Events.md)  
Assembly: DotNetBrowser.dll  

The key location on the keyboard.

```csharp
public enum KeyLocation
```

### Fields

`Left = 3` 

The key location is on the left-hand side of the keyboard (e.g. the left Shift key).



`NumericKeypad = 2` 

The key location is on the numeric keypad or is a virtual key associated with the numeric keypad.



`Right = 4` 

The key location is on the right-hand side of the keyboard (e.g. the right Shift key).



`Standard = 1` 

The key location is not specified or the key is not distinguished from left and right.
