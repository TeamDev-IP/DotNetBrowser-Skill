# <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs"></a> Class NavigationFinishedEventArgs

Namespace: [DotNetBrowser.Navigation.Events](DotNetBrowser.Navigation.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Navigation.INavigation.NavigationFinished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class NavigationFinishedEventArgs : FrameNavigationEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NavigationEventArgs](DotNetBrowser.Navigation.Events.NavigationEventArgs.md) ← 
[FrameNavigationEventArgs](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md) ← 
[NavigationFinishedEventArgs](DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.md)

#### Inherited Members

[FrameNavigationEventArgs.Frame](DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_FrameNavigationEventArgs\_Frame), 
[NavigationEventArgs.Browser](DotNetBrowser.Navigation.Events.NavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_NavigationEventArgs\_Browser), 
[NavigationEventArgs.Navigation](DotNetBrowser.Navigation.Events.NavigationEventArgs.md\#DotNetBrowser\_Navigation\_Events\_NavigationEventArgs\_Navigation), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_ErrorCode"></a> ErrorCode

Gets the navigation error code.

```csharp
public NetError ErrorCode { get; }
```

#### Property Value

 [NetError](DotNetBrowser.Net.NetError.md)

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_HasCommitted"></a> HasCommitted

Indicates whether the navigation has committed.

```csharp
public bool HasCommitted { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_IsErrorPage"></a> IsErrorPage

Indicates whether the navigation resulted in an error page.

```csharp
public bool IsErrorPage { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_IsSameDocument"></a> IsSameDocument

Indicates whether the navigation has been performed in the scope of the same document.

```csharp
public bool IsSameDocument { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_ResponseCode"></a> ResponseCode

The HTTP status code returned by the server in response to the navigation request.

```csharp
public int ResponseCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Remarks

This property is populated when the navigation results in a response that includes valid
response headers.

<p>
    <b>This includes the following cases:</b>
</p>
<ul><li>
            The server returns HTTP(S) response headers with a status code (e.g., 200, 404).
        </li><li>
            Chromium creates a synthetic response header for a well-formed <code>data:</code> URL
            (for example, <code>data:,Hello</code>). In this case, the status code is typically 200 (OK).
        </li><li>
            Chromium creates a response header for a valid <code>file:</code> URL if the file exists,
            also typically with status code 200 (OK).
        </li></ul>

If the navigation does not result in a response with headers, this field is set to 0.

<p>
    <b>This includes the following cases:</b>
</p>
<ul><li>
            The navigation failed at the network level (e.g., DNS failure, timeout, connection refused, offline).
        </li><li>
            The navigation failed due to invalid scheme target URLs:

<ul><li>
                        Malformed <code>data:</code> URLs (e.g., missing comma or invalid format). No synthetic header is
                        created.
                    </li><li>
                        <code>file:</code> URL for a file that does not exist. No synthetic header is created.
                    </li></ul>
        </li><li>
            The target URL uses a scheme that does not involve an HTTP(S) response and therefore
            does not produce response headers, including:

<ul><li><code>about:</code> (e.g., <code>about:blank</code>)</li><li><code>chrome:</code>, <code>chrome-extension:</code> (internal browser/extension pages)</li></ul>
        </li><li>
            The navigation was performed within the same document:

<ul><li>Fragment navigations (e.g., navigating to <code>#anchor</code>)</li><li>History API navigations (e.g., <code>pushState</code>, <code>replaceState</code>)</li></ul>
        </li></ul>
<p>
    <b>Note:</b> A value of <code>0</code> does <b>not</b> mean the server responded with HTTP status code 0.
    It means that the HTTP status code could not be determined because no HTTP-level response occurred
    or no synthetic response was generated for the navigation.
</p>

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_Url"></a> Url

Gets the navigation URL.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Navigation_Events_NavigationFinishedEventArgs_WasServerRedirect"></a> WasServerRedirect

Indicates whether the navigation has encountered a server redirect.

```csharp
public bool WasServerRedirect { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

