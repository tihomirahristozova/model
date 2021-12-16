---
uid: Finance.Payments.PaymentTransactionLines
---
# Finance.Payments.PaymentTransactionLines Entity

**Namespace:** [Finance.Payments](Finance.Payments.md)  

Contains the distibution of the payments' amounts among the source payment orders. Entity: Cash_Payment_Transaction_Lines

## Default Visualization
Default Display Text Format:  
_{PaymentTransaction.EntityName}_  
Default Search Members:  
_PaymentTransaction.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md)  
Aggregate Root:  
[Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowOverpayment](Finance.Payments.PaymentTransactionLines.md#allowoverpayment) | boolean | True-Allows overpayment for the payment order; false=Does not allow (default). `Required` `Default(false)` 
| [Amount](Finance.Payments.PaymentTransactionLines.md#amount) | [Amount (10, 2)](../data-types.md#amount) | The part of the total payed amount by the transaction, that is distributed to the specified payment order. `Currency: PaymentTransaction.TotalAmountCurrency` `Required` `Default(0)` 
| [CoveredOrderAmount](Finance.Payments.PaymentTransactionLines.md#coveredorderamount) | [Amount (10, 2)](../data-types.md#amount) | The part of the original payment order amount, that is covered by this transaction line. `Currency: PaymentOrder.TotalAmountCurrency` `Required` `Default(0)` 
| [Id](Finance.Payments.PaymentTransactionLines.md#id) | guid |  
| [Notes](Finance.Payments.PaymentTransactionLines.md#notes) | string (254) __nullable__ | Notes for this PaymentTransactionLine. 
| [RowVersion](Finance.Payments.PaymentTransactionLines.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Finance.Payments.PaymentTransactionLines.md#document) | [PaymentTransactions](Finance.Payments.PaymentTransactions.md) | The <see cref="PaymentTransaction"/<br />> to which this PaymentTransactionLine belongs. `Required` `Filter(multi eq)` |
| [PaymentOrder](Finance.Payments.PaymentTransactionLines.md#paymentorder) | [PaymentOrders](Finance.Payments.PaymentOrders.md) | The payment order, that is covered by this transaction amount distribution (tr.line). `Required` `Filter(multi eq)` |
| [PaymentTransaction](Finance.Payments.PaymentTransactionLines.md#paymenttransaction) | [PaymentTransactions](Finance.Payments.PaymentTransactions.md) | The <see cref="PaymentTransaction"/<br />> to which this PaymentTransactionLine belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### AllowOverpayment

True-Allows overpayment for the payment order; false=Does not allow (default). `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Amount

The part of the total payed amount by the transaction, that is distributed to the specified payment order. `Currency: PaymentTransaction.TotalAmountCurrency` `Required` `Default(0)`

_Type_: **[Amount (10, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CoveredOrderAmount.ConvertTo( obj.PaymentTransaction.TotalAmountCurrency, obj.PaymentTransaction.CurrencyDirectory)`
### CoveredOrderAmount

The part of the original payment order amount, that is covered by this transaction line. `Currency: PaymentOrder.TotalAmountCurrency` `Required` `Default(0)`

_Type_: **[Amount (10, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.Amount.ConvertTo( obj.PaymentOrder.TotalAmountCurrency, obj.PaymentTransaction.CurrencyDirectory)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this PaymentTransactionLine.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The <see cref="PaymentTransaction"/> to which this PaymentTransactionLine belongs. `Required` `Filter(multi eq)`

_Type_: **[PaymentTransactions](Finance.Payments.PaymentTransactions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentOrder

The payment order, that is covered by this transaction amount distribution (tr.line). `Required` `Filter(multi eq)`

_Type_: **[PaymentOrders](Finance.Payments.PaymentOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentTransaction

The <see cref="PaymentTransaction"/> to which this PaymentTransactionLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[PaymentTransactions](Finance.Payments.PaymentTransactions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentTransactionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentTransactionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentTransactionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentTransactionLines?$top=10>

