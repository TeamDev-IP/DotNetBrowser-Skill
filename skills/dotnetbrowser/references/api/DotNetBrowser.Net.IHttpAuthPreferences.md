# <a id="DotNetBrowser_Net_IHttpAuthPreferences"></a> Interface IHttpAuthPreferences

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The HTTP authorization preferences.

```csharp
public interface IHttpAuthPreferences
```

## Properties

### <a id="DotNetBrowser_Net_IHttpAuthPreferences_DelegateWhiteList"></a> DelegateWhiteList

Gets or sets the HTTP network delegate authorization white list of URLs.
By default, network delegate white list is empty.

```csharp
string DelegateWhiteList { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.IHttpAuthPreferences" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Net_IHttpAuthPreferences_ServerWhiteList"></a> ServerWhiteList

Gets or sets the server HTTP authorization white list of URLs.
By default, server white list is empty.

```csharp
string ServerWhiteList { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Net.IHttpAuthPreferences" data-throw-if-not-resolved="false"></xref> object has already been disposed.

