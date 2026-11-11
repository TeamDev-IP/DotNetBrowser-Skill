# <a id="DotNetBrowser_Card_Handlers"></a> Namespace DotNetBrowser.Card.Handlers

### Classes

 [SaveCreditCardParameters](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardParameters)

The parameters of the <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

 [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardResponse)

A response to the <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Card_Handlers_SaveCreditCardParameters"></a> Class SaveCreditCardParameters

Namespace: [DotNetBrowser.Card.Handlers](DotNetBrowser.Card.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveCreditCardParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Card_Handlers_SaveCreditCardParameters_CreditCard"></a> CreditCard

Gets the credit card that the user entered in the web form.

```csharp
public CreditCard CreditCard { get; }
```

##### Property Value

 [CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

## <a id="DotNetBrowser_Card_Handlers_SaveCreditCardResponse"></a> Class SaveCreditCardResponse

Namespace: [DotNetBrowser.Card.Handlers](DotNetBrowser.Card.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class SaveCreditCardResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SaveCreditCardResponse](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Card_Handlers_SaveCreditCardResponse_Decline"></a> Decline

Creates a <xref href="DotNetBrowser.Card.Handlers.SaveCreditCardResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to decline
to save the credit card.

```csharp
public static SaveCreditCardResponse Decline
```

##### Field Value

 [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardResponse)

#### <a id="DotNetBrowser_Card_Handlers_SaveCreditCardResponse_Save"></a> Save

Creates a <xref href="DotNetBrowser.Card.Handlers.SaveCreditCardResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to save
the credit card to the <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> credit card store.

```csharp
public static SaveCreditCardResponse Save
```

##### Field Value

 [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardResponse)
