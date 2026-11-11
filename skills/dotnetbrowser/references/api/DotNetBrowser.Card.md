# <a id="DotNetBrowser_Card"></a> Namespace DotNetBrowser.Card

### Namespaces

 [DotNetBrowser.Card.Handlers](DotNetBrowser.Card.Handlers.md)

### Classes

 [CreditCard.Builder](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard_Builder)

A builder for creating a new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance.

 [CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

The credit card information persisted in <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> the credit card store.

### Interfaces

 [ICreditCardStore](DotNetBrowser.Card.md#DotNetBrowser_Card_ICreditCardStore)

A service that allows working with <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> credit cards in
the Chromium credit cards store.

 [ICreditCards](DotNetBrowser.Card.md#DotNetBrowser_Card_ICreditCards)

A service that allows managing credit cards.

### Enums

 [CreditCardNetworkType](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCardNetworkType)

The type of the credit card network.

## <a id="DotNetBrowser_Card_CreditCard"></a> Class CreditCard

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

The credit card information persisted in <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> the credit card store.

```csharp
public sealed class CreditCard
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Card_CreditCard_Cardholder"></a> Cardholder

Gets the name of the cardholder entered by the user.

```csharp
public string Cardholder { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Card_CreditCard_ExpirationMonth"></a> ExpirationMonth

Gets the expiration month of the credit card.

```csharp
public int ExpirationMonth { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Remarks

The value may be between 1 and 12.

#### <a id="DotNetBrowser_Card_CreditCard_ExpirationYear"></a> ExpirationYear

Gets the expiration year of the credit card.

```csharp
public int ExpirationYear { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Card_CreditCard_Network"></a> Network

Gets the payment network type of the card.

```csharp
public CreditCardNetworkType Network { get; }
```

##### Property Value

 [CreditCardNetworkType](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCardNetworkType)

#### <a id="DotNetBrowser_Card_CreditCard_Number"></a> Number

Gets the card number.

```csharp
public string Number { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Card_CreditCard_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Card_CreditCard_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Card_CreditCard_Builder"></a> Class CreditCard.Builder

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class CreditCard.Builder
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreditCard.Builder](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard_Builder)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Card_CreditCard_Builder__ctor_System_String_System_Int32_System_Int32_"></a> Builder\(string, int, int\)

Initializes a new instance of the <xref href="DotNetBrowser.Card.CreditCard.Builder" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Builder(string number, int expirationMonth, int expirationYear)
```

##### Parameters

`number` [string](https://learn.microsoft.com/dotnet/api/system.string)

The card number.

`expirationMonth` [int](https://learn.microsoft.com/dotnet/api/system.int32)

`expirationYear` [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Properties

#### <a id="DotNetBrowser_Card_CreditCard_Builder_Cardholder"></a> Cardholder

Gets or sets the name of the cardholder entered by the user.

```csharp
public string Cardholder { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Card_CreditCard_Builder_ExpirationMonth"></a> ExpirationMonth

Gets the expiration month of the credit card.

```csharp
public int ExpirationMonth { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Card_CreditCard_Builder_ExpirationYear"></a> ExpirationYear

Gets the expiration year of the credit card.

```csharp
public int ExpirationYear { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Card_CreditCard_Builder_Number"></a> Number

Gets the card number.

```csharp
public string Number { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Card_CreditCard_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance with the properties set in the builder.

```csharp
public CreditCard Build()
```

##### Returns

 [CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

A new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Card_ICreditCardStore"></a> Interface ICreditCardStore

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A service that allows working with <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> credit cards in
the Chromium credit cards store.

```csharp
public interface ICreditCardStore
```

### Properties

#### <a id="DotNetBrowser_Card_ICreditCardStore_All"></a> All

Gets all records from the credit cards store.

```csharp
IReadOnlyList<CreditCard> All { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)\>

##### Remarks

Credit card records are saved to the store via <xref href="DotNetBrowser.Card.ICreditCards.SaveCreditCardHandler" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Card_ICreditCardStore_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated wit this <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref>.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

### Methods

#### <a id="DotNetBrowser_Card_ICreditCardStore_Add_DotNetBrowser_Card_CreditCard_"></a> Add\(CreditCard\)

Adds the credit card to the store.

```csharp
void Add(CreditCard creditCard)
```

##### Parameters

`creditCard` [CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

The credit card associated with the removed credit card records.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">creditCard</code> is null, or there is a card validation failure.

#### <a id="DotNetBrowser_Card_ICreditCardStore_Clear"></a> Clear\(\)

Clears all records in the store.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Card_ICreditCardStore_Remove_DotNetBrowser_Card_CreditCard_"></a> Remove\(CreditCard\)

Removes the credit card from the store.

```csharp
void Remove(CreditCard creditCard)
```

##### Parameters

`creditCard` [CreditCard](DotNetBrowser.Card.md#DotNetBrowser_Card_CreditCard)

The credit card associated with the removed credit card records.

##### Remarks

Removed credit cards are not displayed in the autofill suggestion pop-up.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">creditCard</code> is null.

## <a id="DotNetBrowser_Card_ICreditCards"></a> Interface ICreditCards

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A service that allows managing credit cards.

```csharp
public interface ICreditCards : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Card_ICreditCards_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Card_ICreditCards_SaveCreditCardHandler"></a> SaveCreditCardHandler

Gets or sets a handler that is used when the user is prompted to save a credit card to the
<xref href="DotNetBrowser.Card.ICreditCardStore?text=%0a++++++++++++credit+card+store%0a++++++++" data-throw-if-not-resolved="false"></xref>

```csharp
IHandler<SaveCreditCardParameters, SaveCreditCardResponse> SaveCreditCardHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardParameters), [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Card.ICreditCards" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Card_CreditCardNetworkType"></a> Enum CreditCardNetworkType

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

The type of the credit card network.

```csharp
public enum CreditCardNetworkType
```

### Fields

`AmericanExpress = 2` 

The AmericanExpress network type.



`Diners = 3` 

The Diners network type.



`Discover = 4` 

The Discover network type.



`Elo = 5` 

The Elo network type.



`Generic = 6` 

The Generic network type.



`Jcb = 7` 

The Jcb network type.



`MasterCard = 8` 

The MasterCard network type.



`Mir = 9` 

The Mir network type.



`Troy = 10` 

The Troy network type.



`UnionPay = 11` 

The UnionPay network type.



`Unknown = 1` 

Unknown credit card network type.



`Visa = 12` 

The Visa network type.
