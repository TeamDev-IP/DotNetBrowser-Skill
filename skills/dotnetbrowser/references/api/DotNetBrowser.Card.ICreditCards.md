# <a id="DotNetBrowser_Card_ICreditCards"></a> Interface ICreditCards

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing credit cards.

```csharp
public interface ICreditCards : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Card_ICreditCards_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Card_ICreditCards_SaveCreditCardHandler"></a> SaveCreditCardHandler

Gets or sets a handler that is used when the user is prompted to save a credit card to the
<xref href="DotNetBrowser.Card.ICreditCardStore?text=%0a++++++++++++credit+card+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<SaveCreditCardParameters, SaveCreditCardResponse> SaveCreditCardHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.SaveCreditCardParameters.md), [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.SaveCreditCardResponse.md)\>

#### Remarks

<p>
    The callback is invoked when the user submits a form with credit card information
    (a cardholder name, number, expiration date, CVV/CVC).
</p>
<p>
    This callback is equivalent to the "Save Card?" bubble in Chromium.
</p>
<p>
    Use the <xref href="DotNetBrowser.Card.Handlers.SaveCreditCardResponse.Save" data-throw-if-not-resolved="false"></xref> to save the credit card to the
    <xref href="DotNetBrowser.Card.ICreditCardStore?text=credit+card+store" data-throw-if-not-resolved="false"></xref>. All saved credit cards are shown
    in the suggestion pop-up when focusing the web form control.
</p>
<p>
    Use the <xref href="DotNetBrowser.Card.Handlers.SaveCreditCardResponse.Decline" data-throw-if-not-resolved="false"></xref> to decline to save the credit card. If the
    current credit card is declined then the callback will be invoked again when submitting a
    web form with the same credit card.
</p>
<p>
    The handler is not invoked if <xref href="DotNetBrowser.Profile.IProfilePreferences.AutofillEnabled?text=autofill" data-throw-if-not-resolved="false"></xref> is disabled.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCards" data-throw-if-not-resolved="false"></xref> has already been disposed.

