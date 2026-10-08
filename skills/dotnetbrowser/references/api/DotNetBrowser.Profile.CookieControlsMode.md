# <a id="DotNetBrowser_Profile_CookieControlsMode"></a> Enum CookieControlsMode

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The Chromium third-party cookies block mode.

```csharp
public enum CookieControlsMode
```

## Fields

`BlockThirdParty = 2` 

Sites can't use user cookies to see user browsing activity across different sites, for example, to personalize ads.
Features on some sites may not work.



`IncognitoOnly = 3` 

While in Incognito, sites can't use user cookies to see user browsing activity across sites, even related sites.
The user browsing activity isn't used for things like personalizing ads. Features on some sites may not work.



`Off = 1` 

Sites can use cookies to see the user browsing activity across different sites, for example, to personalize ads.



`Undefined = 0` 

Reserved value.



