# <a id="DotNetBrowser_Card_CreditCard"></a> Class CreditCard

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

The credit card information persisted in <xref href="DotNetBrowser.Card.ICreditCardStore" data-throw-if-not-resolved="false"></xref> the credit card store.

```csharp
public sealed class CreditCard
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreditCard](DotNetBrowser.Card.CreditCard.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Card_CreditCard_Cardholder"></a> Cardholder

Gets the name of the cardholder entered by the user.

```csharp
public string Cardholder { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Card_CreditCard_ExpirationMonth"></a> ExpirationMonth

Gets the expiration month of the credit card.

```csharp
public int ExpirationMonth { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Remarks

The value may be between 1 and 12.

### <a id="DotNetBrowser_Card_CreditCard_ExpirationYear"></a> ExpirationYear

Gets the expiration year of the credit card.

```csharp
public int ExpirationYear { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Card_CreditCard_Network"></a> Network

Gets the payment network type of the card.

```csharp
public CreditCardNetworkType Network { get; }
```

#### Property Value

 [CreditCardNetworkType](DotNetBrowser.Card.CreditCardNetworkType.md)

### <a id="DotNetBrowser_Card_CreditCard_Number"></a> Number

Gets the card number.

```csharp
public string Number { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Card_CreditCard_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Card_CreditCard_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

