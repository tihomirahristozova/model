---
uid: data-types
---
# Data Types

## Simple Types

## Complex Types

### MultilanguageString

Multi-language strings - https://enterpriseone.atlassian.net/wiki/display/techdoc/Multi-language

Some text properties support value in more than one language. This properties are of multi-language string type.

Example: General_Products_Products.Name property.

The multi-language string can store many language strings, indexing them by language key. The language key is a CultureInfo two letter ISO language name, like "en", "de", etc.

For example the Name property of General_Products_Products entity is displayed as:
<code>
{
  "Name": {
	  "bg": "Ябълка",
	  "en": "Apple"
  }
}
<code>

>ALL multi-language values are treated as a single value. You cannot GET/PUT/PATCH only some multi-language values - they are treated as a single piece of data.

> **Note!**  
> Multi-language properties support only filter function **contains**:  
> Domain API: 
> ~/General_Products_Products?$filter=contains(Name,'ppl')  
> This is an invalid filter:  
> ~/General_Products_Products?$filter=Name eq 'Apple'  

### Amount

The ERP domain model declares a special type for amount (currency) properties.

The amount is represented by value and currency.

| Name | Type | Description |
| --- | --- | --- |
| Currency | String | The currency of the amount represented by it's sign. |
| Value | Decimal | The value of the amount. |

Domain API Example:  
Example:

{
  "LineAmount": {
    "Value": "3.55",
    "Currency": "USD"
  }
}

### Quantity

The ERP domain model declares a special type for quantity properties.

The quantity is represented by value and measurement unit.

| Name | Type | Description |
| --- | --- | --- |
| Unit | String | TThe measurement unit of the quantity represented by it's code. |
| Value | Decimal | The value of the quantity. |

Domain API Example:  
Example:

{
  "LineAmount": {
    "Value": "5.555",
    "Unit": "PCS"
  }
}

### CustomPropertyValue
