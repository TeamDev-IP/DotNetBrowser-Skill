# <a id="DotNetBrowser_Card_ICreditCardStore"></a> Interface ICreditCardStore

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A service that allows working with <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> credit cards in
the Chromium credit cards store.

```csharp
public interface ICreditCardStore
```

## Properties

### <a id="DotNetBrowser_Card_ICreditCardStore_All"></a> All

Gets all records from the credit cards store.

```csharp
IReadOnlyList<CreditCard> All { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[CreditCard](DotNetBrowser.Card.CreditCard.md)\>

#### Remarks

Credit card records are saved to the store via <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Card_ICreditCardStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated wit this <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Card_ICreditCardStore_Add_DotNetBrowser_Card_CreditCard_"></a> Add\(CreditCard\)

Adds the credit card to the store.

```csharp
void Add(CreditCard creditCard)
```

#### Parameters

`creditCard` [CreditCard](DotNetBrowser.Card.CreditCard.md)

The credit card associated with the removed credit card records.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">creditCard</code> is null, or there is a card validation failure.

### <a id="DotNetBrowser_Card_ICreditCardStore_Clear"></a> Clear\(\)

Clears all records in the store.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Card_ICreditCardStore_Remove_DotNetBrowser_Card_CreditCard_"></a> Remove\(CreditCard\)

Removes the credit card from the store.

```csharp
void Remove(CreditCard creditCard)
```

#### Parameters

`creditCard` [CreditCard](DotNetBrowser.Card.CreditCard.md)

The credit card associated with the removed credit card records.

#### Remarks

Removed credit cards are not displayed in the autofill suggestion pop-up.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">creditCard</code> is null.

