# <a id="DotNetBrowser_Browser_PreferredColorScheme"></a> Enum PreferredColorScheme

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The preferred color scheme for the web content in the browser.

```csharp
public enum PreferredColorScheme
```

## Fields

`Dark = 1` 

The dark color scheme is preferred.



`Light = 2` 

The light color scheme is preferred.



## Remarks

The scheme is used to evaluate the <code>prefers-color-scheme</code> media query and resolve UA color scheme to be used
based on the <code>supported-color-schemes</code> META tag and CSS property.

