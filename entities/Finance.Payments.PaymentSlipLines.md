# Finance.Payments.PaymentSlipLines

Mass payment line, which is distribution of an amount among payment orders. Each record generates one payment transaction line. Entity: Cash_Payment_Slip_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Payments.PaymentSlipLines.md#Id) | guid |  
| [Amount](Finance.Payments.PaymentSlipLines.md#Amount) | [Amount](../data-types/Amount.md) | The part of the total amount in the payment slip amount, that is distributed to the specified payment order. [Currency: PaymentSlipAmount.PaymentSlip.DocumentCurrency] [Required] [Default(0)] 
| [CoveredOrderAmount](Finance.Payments.PaymentSlipLines.md#CoveredOrderAmount) | [Amount](../data-types/Amount.md) | The part of the original payment order amount, that is covered by this payment slip line. [Currency: PaymentOrder.TotalAmountCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PaymentOrder](Finance.Payments.PaymentSlipLines.md#PaymentOrder) | [Finance.Payments.PaymentOrders](Finance.Payments.PaymentOrders.md) | The payment order, that is covered by this payment slip line. [Required] [Filter(multi eq)] |
| [PaymentSlipAmount](Finance.Payments.PaymentSlipLines.md#PaymentSlipAmount) | [Finance.Payments.PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md) | The [PaymentSlipAmount](Finance.Payments.PaymentSlipLines.md#PaymentSlipAmount) to which this PaymentSlipLine belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Amount

> The part of the total amount in the payment slip amount, that is distributed to the specified payment order. [Currency: PaymentSlipAmount.PaymentSlip.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CoveredOrderAmount.ConvertTo(obj.PaymentSlipAmount.PaymentSlip.DocumentCurrency, obj.PaymentSlipAmount.PaymentSlip.CurrencyDirectory)`
### CoveredOrderAmount

> The part of the original payment order amount, that is covered by this payment slip line. [Currency: PaymentOrder.TotalAmountCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.Amount.ConvertTo(obj.PaymentOrder.TotalAmountCurrency, obj.PaymentSlipAmount.PaymentSlip.CurrencyDirectory)`

## Reference Details

### PaymentOrder

> The payment order, that is covered by this payment slip line. [Required] [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentOrders](Finance.Payments.PaymentOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PaymentSlipAmount

> The [PaymentSlipAmount](Finance.Payments.PaymentSlipLines.md#PaymentSlipAmount) to which this PaymentSlipLine belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[Finance.Payments.PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Payments.PaymentSlipLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentSlipLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentSlipLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentSlipLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentSlipLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cash_Payment_Slip_Lines?$top=10>

