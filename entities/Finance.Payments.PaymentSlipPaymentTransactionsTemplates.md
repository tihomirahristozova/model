# Finance.Payments.PaymentSlipPaymentTransactionsTemplates

Contains options for generation of payment transactions. Each option set is assigned to specific generation route. Entity: Cash_Payment_Slip_Payment_Transactions_Templates (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#Id) | guid |  
| [CreateExpensePayments](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#CreateExpensePayments) | boolean | True if the generation creates payment transactions for Payment Slip Amounts with direction Expense. [Required] [Filter(eq)] 
| [CreateIncomePayments](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#CreateIncomePayments) | boolean | True if the generation creates payment transactions for Payment Slip Amounts with direction Income. [Required] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#Route) | [Systems.Workflow.Routes](Systems.Workflow.Routes.md) | The route to which the current option set is assigned. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CreateExpensePayments

> True if the generation creates payment transactions for Payment Slip Amounts with direction Expense. [Required] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### CreateIncomePayments

> True if the generation creates payment transactions for Payment Slip Amounts with direction Income. [Required] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### Route

> The route to which the current option set is assigned. [Required] [Filter(multi eq)]

_Type_: **[Systems.Workflow.Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cash_Payment_Slip_Payment_Transactions_Templates?$top=10>

