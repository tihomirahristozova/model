---
uid: Finance.Payments.PaymentSlipPaymentTransactionsTemplates
---
# Finance.Payments.PaymentSlipPaymentTransactionsTemplates Entity

**Namespace:** [Finance.Payments](Finance.Payments.md)  

Contains options for generation of payment transactions. Each option set is assigned to specific generation route. Entity: Cash_Payment_Slip_Payment_Transactions_Templates (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Id}: {RouteId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Payments.PaymentSlipPaymentTransactionsTemplates](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreateExpensePayments](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#createexpensepayments) | boolean | True if the generation creates payment transactions for Payment Slip Amounts with direction Expense. `Required` `Filter(eq)` 
| [CreateIncomePayments](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#createincomepayments) | boolean | True if the generation creates payment transactions for Payment Slip Amounts with direction Income. `Required` `Filter(eq)` 
| [Id](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#id) | guid |  
| [RowVersion](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#route) | [Routes](Systems.Workflow.Routes.md) | The route to which the current option set is assigned. `Required` `Filter(multi eq)` |


## Attribute Details

### CreateExpensePayments

True if the generation creates payment transactions for Payment Slip Amounts with direction Expense. `Required` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### CreateIncomePayments

True if the generation creates payment transactions for Payment Slip Amounts with direction Income. `Required` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Route

The route to which the current option set is assigned. `Required` `Filter(multi eq)`

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

