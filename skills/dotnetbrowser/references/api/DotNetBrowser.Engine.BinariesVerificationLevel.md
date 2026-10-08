# <a id="DotNetBrowser_Engine_BinariesVerificationLevel"></a> Enum BinariesVerificationLevel

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The level of the Chromium binaries verification.

```csharp
public enum BinariesVerificationLevel
```

## Fields

`Minimal = 1` 

Check files presence only.



`Normal = 2` 

Check files presence and size.



`Off = 0` 

Do not perform binaries verification.



`Strong = 3` 

Check files presence and hash.

Calculating hash is a time-consuming operation, so this check slows down the engine initialization.

