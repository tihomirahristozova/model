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
| [DisplayText](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#id) | guid |  
| [ObjectVersion](Finance.Payments.PaymentSlipPaymentTransactionsTemplates.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 

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

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Route

The route to which the current option set is assigned. `Required` `Filter(multi eq)`

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  


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

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Payments.PaymentSlipPaymentTransactionsTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentSlipPaymentTransactionsTemplates?$top=10>

