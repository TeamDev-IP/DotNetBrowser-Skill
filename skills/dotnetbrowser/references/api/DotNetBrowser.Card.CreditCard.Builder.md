# <a id="DotNetBrowser_Card_CreditCard_Builder"></a> Class CreditCard.Builder

Namespace: [DotNetBrowser.Card](DotNetBrowser.Card.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class CreditCard.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreditCard.Builder](DotNetBrowser.Card.CreditCard.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Card_CreditCard_Builder__ctor_System_String_System_Int32_System_Int32_"></a> Builder\(string, int, int\)

Initializes a new instance of the <xref href="DotNetBrowser.Card.CreditCard.Builder" data-throw-if-not-resolved="false"></xref> class.

```csharp
public Builder(string number, int expirationMonth, int expirationYear)
```

#### Parameters

`number` [string](https://learn.microsoft.com/dotnet/api/system.string)

The card number.

`expirationMonth` [int](https://learn.microsoft.com/dotnet/api/system.int32)

`expirationYear` [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Properties

### <a id="DotNetBrowser_Card_CreditCard_Builder_Cardholder"></a> Cardholder

Gets or sets the name of the cardholder entered by the user.

```csharp
public string Cardholder { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Card_CreditCard_Builder_ExpirationMonth"></a> ExpirationMonth

Gets the expiration month of the credit card.

```csharp
public int ExpirationMonth { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Card_CreditCard_Builder_ExpirationYear"></a> ExpirationYear

Gets the expiration year of the credit card.

```csharp
public int ExpirationYear { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Card_CreditCard_Builder_Number"></a> Number

Gets the card number.

```csharp
public string Number { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Card_CreditCard_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance with the properties set in the builder.

```csharp
public CreditCard Build()
```

#### Returns

 [CreditCard](DotNetBrowser.Card.CreditCard.md)

A new <xref href="DotNetBrowser.Card.CreditCard" data-throw-if-not-resolved="false"></xref> instance.

