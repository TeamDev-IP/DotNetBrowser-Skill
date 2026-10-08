# <a id="DotNetBrowser_Dom_Events_IUiKeyEventModifier"></a> Interface IUiKeyEventModifier

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents a DOM UI event that can be fired with the key modifiers.

<p>
    The <xref href="DotNetBrowser.Dom.Events.IUiKeyEventModifier.KeyModifiers" data-throw-if-not-resolved="false"></xref> provides access to the data about pressed service keys, such as
    <code>Ctrl</code>, <code>Alt</code>, <code>Shift</code>, <code>Meta</code>,
    when a keyboard or mouse event occurs.
</p>

```csharp
public interface IUiKeyEventModifier : IEvent, IAutoDisposable
```

#### Implements

[IEvent](DotNetBrowser.Dom.Events.IEvent.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_IUiKeyEventModifier_KeyModifiers"></a> KeyModifiers

Gets the key modifiers that are applied to the event.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

