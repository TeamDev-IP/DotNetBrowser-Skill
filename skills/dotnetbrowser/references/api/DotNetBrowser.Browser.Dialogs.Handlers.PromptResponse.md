# <a id="DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse"></a> Class PromptResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.PromptHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class PromptResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PromptResponse](DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse_Canceled"></a> Canceled

Indicates whether the prompt dialog has been canceled.

```csharp
public bool Canceled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse_Text"></a> Text

Gets the text input entered in the prompt dialog.

```csharp
public string Text { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the prompt dialog has been canceled.

```csharp
public static PromptResponse Cancel()
```

#### Returns

 [PromptResponse](DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.PromptHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse_SubmitText_System_String_"></a> SubmitText\(string\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the user input was submitted in the prompt
dialog.

```csharp
public static PromptResponse SubmitText(string text)
```

#### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

The user input that was submitted in the prompt dialog.

#### Returns

 [PromptResponse](DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.PromptHandler" data-throw-if-not-resolved="false"></xref> implementation.

