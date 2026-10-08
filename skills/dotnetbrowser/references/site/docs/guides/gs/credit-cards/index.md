
# Credit cards

**Lead**
This guide describes how to save, update and manage credit cards.


## Overview

Chromium has built-in functionality that allows remembering credit cards entered into web forms. When the user submits a web form containing credit card info then the library will ask whether to save it to the credit card store.

If you save it, the next time you load the form, the library will suggest to autofill it.

![Card](https://teamdev.com/dotnetbrowser/img/releases/2-14/card.webp)

## Saving credit cards

When the user submits a form containing credit card info (a cardholder name, number, expiration date, CVV/CVC), the library will ask you if you’d like to save the card via `SaveCreditCardHandler`. In the handler, you will be prompted to save or decline the card. For example:


**C#**
```csharp
Browser.CreditCards.SaveCreditCardHandler = 
    new Handler<SaveCreditCardParameters, SaveCreditCardResponse>(
        p => SaveCreditCardResponse.Save);
```

**VB**
```vb
Browser.CreditCards.SaveCreditCardHandler = 
    New Handler(Of SaveCreditCardParameters, SaveCreditCardResponse)
        (Function(p) SaveCreditCardResponse.Save)
```



If you choose to save, this card will be added to the credit card store. Next time you enter the same credit card to a form the callback will not be invoked.

If you choose to decline the card, it will not be added to the store and next time when entering the exact same credit card the callback will be invoked again.

## Managing credit cards

Each record in the credit card store is represented by a separate object of `CreditCard`. It contains cardholder name, number, expiration date, etc.

To read all records, use `ICreditCardStore`:


**C#**
```csharp
IReadOnlyList<CreditCard> allCreditCards = 
    Engine.Profiles.Default.CreditCardStore.All;
```

**VB**
```vb
Dim allCreditCards As IReadOnlyList(Of CreditCard) = 
    Engine.Profiles.Default.CreditCardStore.All
```



To remove any record from the store, use:


**C#**
```csharp
Engine.Profiles.Default.CreditCardStore.Remove(creditCard);
```

**VB**
```vb
Engine.Profiles.Default.CreditCardStore.Remove(creditCard)
```



To clear all credit cards, use the following method:


**C#**
```csharp
Engine.Profiles.Default.CreditCardStore.Clear();
```

**VB**
```vb
Engine.Profiles.Default.CreditCardStore.Clear()
```


