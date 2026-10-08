# <a id="DotNetBrowser_Profile_IProfilePreferences"></a> Interface IProfilePreferences

Namespace: [DotNetBrowser.Profile](DotNetBrowser.Profile.md)  
Assembly: DotNetBrowser.dll  

The preferences of a <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IProfilePreferences : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Profile_IProfilePreferences_AutofillEnabled"></a> AutofillEnabled

Enables or disables the web form autofill and displaying of suggestions pop-ups. By default, the autofill is
enabled.

```csharp
bool AutofillEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    <b>Important:</b> the autofill for the <xref href="DotNetBrowser.Passwords.IPasswordStore" data-throw-if-not-resolved="false"></xref> passwords is always
    enabled except the cases when a site has an invalid SSL certificate or the scheme is not
    registered as web-safe.The list of web-safe schemes: HTTP, HTTPS, WS, and WSS.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Profile_IProfilePreferences_CaretBrowsingEnabled"></a> CaretBrowsingEnabled

Enables or disables the caret browsing. By default, the caret browsing is
disabled.

```csharp
bool CaretBrowsingEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Profile_IProfilePreferences_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Profile_IProfilePreferences_NetworkPredictionEnabled"></a> NetworkPredictionEnabled

Enables or disables the network prediction. By default, the network prediction is enabled.

```csharp
bool NetworkPredictionEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

Network prediction is the built-in feature of Chromium that allows you to open the most visited websites faster.
This is done by DNS prefetching, TCP and SSL preconnection, prerendering of web pages, and resource prefetching.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Profile.IProfilePreferences" data-throw-if-not-resolved="false"></xref> instance has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Profile_IProfilePreferences_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Profile_IProfilePreferences_ThirdPartyCookieMode"></a> ThirdPartyCookieMode

Gets or sets the third-party cookies blocking mode.

```csharp
CookieControlsMode ThirdPartyCookieMode { get; set; }
```

#### Property Value

 [CookieControlsMode](DotNetBrowser.Profile.CookieControlsMode.md)

