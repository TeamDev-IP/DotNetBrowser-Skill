
# Migrating from 2.16.1 to 2.17

**Lead**
This article describes the API changes between versions 2.16.1 and 2.17.


## Updated API

### Fullscreen events

The `FullScreenEntered` and `FullScreenExited` events were replaced with `IFullScreen.Entered` and `IFullScreen.Exited` ones:

**v2.16.1**

```csharp
browser.FullScreenEntered += (sender, e) => {};
browser.FullScreenExited += (sender, e) => {};
```

**v2.17**

```csharp
browser.FullScreen.Entered += (sender, e) => {};
browser.FullScreen.Exited += (sender, e) => {};
```
