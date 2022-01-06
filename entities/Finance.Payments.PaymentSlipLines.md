---
uid: Finance.Payments.PaymentSlipLines
---
# Finance.Payments.PaymentSlipLines Entity

**Namespace:** [Finance.Payments](Finance.Payments.md)  

Mass payment line, which is distribution of an amount among payment orders. Each record generates one payment transaction line. Entity: Cash_Payment_Slip_Lines

## Default Visualization
Default Display Text Format:  
_{PaymentSlipAmount.PartyName:T}_  
Default Search Members:  
_PaymentSlipAmount.PartyName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Payments.PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md)  
Aggregate Root:  
[Finance.Payments.PaymentSlips](Finance.Payments.PaymentSlips.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](Finance.Payments.PaymentSlipLines.md#amount) | [Amount (10, 2)](../data-types.md#amount) | The part of the total amount in the payment slip amount, that is distributed to the specified payment order. `Currency: PaymentSlipAmount.PaymentSlip.DocumentCurrency` `Required` `Default(0)` 
| [CoveredOrderAmount](Finance.Payments.PaymentSlipLines.md#coveredorderamount) | [Amount (10, 2)](../data-types.md#amount) | The part of the original payment order amount, that is covered by this payment slip line. `Currency: PaymentOrder.TotalAmountCurrency` `Required` `Default(0)` 
| [Id](Finance.Payments.PaymentSlipLines.md#id) | guid |  
| [ObjectVersion](Finance.Payments.PaymentSlipLines.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PaymentOrder](Finance.Payments.PaymentSlipLines.md#paymentorder) | [PaymentOrders](Finance.Payments.PaymentOrders.md) | The payment order, that is covered by this payment slip line. `Required` `Filter(multi eq)` |
| [PaymentSlipAmount](Finance.Payments.PaymentSlipLines.md#paymentslipamount) | [PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md) | The <see cref="PaymentSlipAmount"/> to which this PaymentSlipLine belongs. `Required` `Filter(multi eq)` `ReadOnly` `Owner` |


## Attribute Details

### Amount

The part of the total amount in the payment slip amount, that is distributed to the specified payment order. `Currency: PaymentSlipAmount.PaymentSlip.DocumentCurrency` `Required` `Default(0)`

_Type_: **[Amount (10, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CoveredOrderAmount.ConvertTo( obj.PaymentSlipAmount.PaymentSlip.DocumentCurrency, obj.PaymentSlipAmount.PaymentSlip.CurrencyDirectory)`
### CoveredOrderAmount

The part of the original payment order amount, that is covered by this payment slip line. `Currency: PaymentOrder.TotalAmountCurrency` `Required` `Default(0)`

_Type_: **[Amount (10, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.Amount.ConvertTo( obj.PaymentOrder.TotalAmountCurrency, obj.PaymentSlipAmount.PaymentSlip.CurrencyDirectory)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### PaymentOrder

The payment order, that is covered by this payment slip line. `Required` `Filter(multi eq)`

_Type_: **[PaymentOrders](Finance.Payments.PaymentOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentSlipAmount

The <see cref="PaymentSlipAmount"/> to which this PaymentSlipLine belongs. `Required` `Filter(multi eq)` `ReadOnly` `Owner`

_Type_: **[PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentSlipLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentSlipLines?$top=10>

