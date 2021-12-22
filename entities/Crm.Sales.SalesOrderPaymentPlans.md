---
uid: Crm.Sales.SalesOrderPaymentPlans
---
# Crm.Sales.SalesOrderPaymentPlans Entity

**Namespace:** [Crm.Sales](Crm.Sales.md)  

Payment plan of a sales order. Entity: Crm_Sales_Order_Payment_Plans

## Default Visualization
Default Display Text Format:  
_{SalesOrder.EntityName}_  
Default Search Members:  
_SalesOrder.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md)  
Aggregate Root:  
[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](Crm.Sales.SalesOrderPaymentPlans.md#amount) | [Amount (14, 2)](../data-types.md#amount) | Amount to be payed. `Currency: SalesOrder.DocumentCurrency` `Required` 
| [AmountPercent](Crm.Sales.SalesOrderPaymentPlans.md#amountpercent) | decimal (7, 6) __nullable__ | Percent of the sales order amount to be payed. 
| [DueDateFormMethod](Crm.Sales.SalesOrderPaymentPlans.md#duedateformmethod) | [PaymentPlanDueDateSource](Crm.Sales.SalesOrderPaymentPlans.md#duedateformmethod) | Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. `Required` 
| [ExplicitPaymentDueDate](Crm.Sales.SalesOrderPaymentPlans.md#explicitpaymentduedate) | datetime __nullable__ | Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'. 
| [ExplicitPayment<br />DueStartDate](Crm.Sales.SalesOrderPaymentPlans.md#explicitpaymentduestartdate) | date __nullable__ | Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'. 
| [Id](Crm.Sales.SalesOrderPaymentPlans.md#id) | guid |  
| [InstallmentNumber](Crm.Sales.SalesOrderPaymentPlans.md#installmentnumber) | int32 | Consequtive installment number. Used for identifying different payments generated according this payment plan. `Required` 
| [Notes](Crm.Sales.SalesOrderPaymentPlans.md#notes) | string (254) __nullable__ | Notes for this SalesOrderPaymentPlan. 
| [ObjectVersion](Crm.Sales.SalesOrderPaymentPlans.md#objectversion) | int32 |  
| [PaymentStartDays](Crm.Sales.SalesOrderPaymentPlans.md#paymentstartdays) | int32 | Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method. `Required` `Default(0)` 
| [PaymentTermDays](Crm.Sales.SalesOrderPaymentPlans.md#paymenttermdays) | int32 | Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. `Required` `Default(0)` 
| [Remainder](Crm.Sales.SalesOrderPaymentPlans.md#remainder) | boolean | Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount). `Required` `Default(false)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PaymentAccount](Crm.Sales.SalesOrderPaymentPlans.md#paymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | Specifies the payment account towards which the payment is expected. null means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred. `Filter(multi eq)` |
| [PaymentType](Crm.Sales.SalesOrderPaymentPlans.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Specifies the expected payment type. null means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred. `Filter(multi eq)` |
| [SalesOrder](Crm.Sales.SalesOrderPaymentPlans.md#salesorder) | [SalesOrders](Crm.Sales.SalesOrders.md) | The <see cref="SalesOrder"/> to which this SalesOrderPaymentPlan belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Amount

Amount to be payed. `Currency: SalesOrder.DocumentCurrency` `Required`

_Type_: **[Amount (14, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AmountPercent

Percent of the sales order amount to be payed.

_Type_: **decimal (7, 6) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DueDateFormMethod

Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. `Required`

_Type_: **[PaymentPlanDueDateSource](Crm.Sales.SalesOrderPaymentPlans.md#duedateformmethod)**  
Generic enum type for PaymentPlanDueDateSource properties  
_Allowed Values (Crm.PaymentPlanDueDateSource Enum Members)_  

| Value | Description |
| ---- | --- |
| SpecifyTheDateExplicitly | SpecifyTheDateExplicitly value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SpecifyTheDateExplicitly' |
| UseInvoiceDate | UseInvoiceDate value. Stored as 'INV'. <br /> _Database Value:_ 'INV' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'UseInvoiceDate' |
| UseSalesOrderDate | UseSalesOrderDate value. Stored as 'SLS'. <br /> _Database Value:_ 'SLS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'UseSalesOrderDate' |
| UseSalesOrderDueDate | UseSalesOrderDueDate value. Stored as 'SDD'. <br /> _Database Value:_ 'SDD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'UseSalesOrderDueDate' |
| UseInvoiceDueDate | UseInvoiceDueDate value. Stored as 'IDD'. <br /> _Database Value:_ 'IDD' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'UseInvoiceDueDate' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExplicitPaymentDueDate

Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DueDateFormMethod, Int32) != 0), null, obj.ExplicitPaymentDueDate)`
### ExplicitPaymentDueStartDate

Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.

_Type_: **date __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DueDateFormMethod, Int32) != 0), null, obj.ExplicitPaymentDueStartDate)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InstallmentNumber

Consequtive installment number. Used for identifying different payments generated according this payment plan. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.SalesOrder.PaymentPlans.Select( c => c.InstallmentNumber).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.SalesOrder.PaymentPlans.Select( c => c.InstallmentNumber).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this SalesOrderPaymentPlan.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### PaymentStartDays

Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### PaymentTermDays

Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`IIF( ( ( Convert( obj.DueDateFormMethod, Int32) == 3) OrElse ( Convert( obj.DueDateFormMethod, Int32) == 4)), 0, obj.PaymentTermDays)`

_Front-End Recalc Expressions:_  
`IIF( ( ( Convert( obj.DueDateFormMethod, Int32) == 3) OrElse ( Convert( obj.DueDateFormMethod, Int32) == 4)), 0, obj.PaymentTermDays)`
### Remainder

Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount). `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

_Back-End Default Expression:_  
`IIF( ( obj.AmountPercent != null), False, obj.Remainder)`

_Front-End Recalc Expressions:_  
`IIF( ( obj.AmountPercent != null), False, obj.Remainder)`

## Reference Details

### PaymentAccount

Specifies the payment account towards which the payment is expected. null means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred. `Filter(multi eq)`

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesOrder.PaymentAccount`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.PaymentAccount.IfNullThen( obj.PaymentType.DefaultPaymentAccount.IfNullThen( obj.PaymentAccount))`
`obj.SalesOrder.PaymentAccount`
### PaymentType

Specifies the expected payment type. null means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred. `Filter(multi eq)`

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesOrder.PaymentType`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.PaymentType`
### SalesOrder

The <see cref="SalesOrder"/> to which this SalesOrderPaymentPlan belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[SalesOrders](Crm.Sales.SalesOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Sales.SalesOrderPaymentPlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Sales.SalesOrderPaymentPlans erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrderPaymentPlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrderPaymentPlans?$top=10>

