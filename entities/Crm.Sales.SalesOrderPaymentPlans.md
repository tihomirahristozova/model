---
uid: Crm.Sales.SalesOrderPaymentPlans
---
# Crm.Sales.SalesOrderPaymentPlans Entity

Payment plan of a sales order. Entity: Crm_Sales_Order_Payment_Plans

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](Crm.Sales.SalesOrderPaymentPlans.md#amount) | [Amount](../data-types.md#amount) | Amount to be payed. [Currency: SalesOrder.DocumentCurrency] [Required] 
| [AmountPercent](Crm.Sales.SalesOrderPaymentPlans.md#amountpercent) | decimal (nullable) | Percent of the sales order amount to be payed. 
| [DueDateFormMethod](Crm.Sales.SalesOrderPaymentPlans.md#duedateformmethod) | [PaymentPlanDueDateSource](Crm.Sales.SalesOrderPaymentPlans.md#duedateformmethod) | Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. [Required] 
| [ExplicitPaymentDueDate](Crm.Sales.SalesOrderPaymentPlans.md#explicitpaymentduedate) | datetime (nullable) | Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'. 
| [ExplicitPayment<br />DueStartDate](Crm.Sales.SalesOrderPaymentPlans.md#explicitpaymentduestartdate) | date (nullable) | Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'. 
| [Id](Crm.Sales.SalesOrderPaymentPlans.md#id) | guid |  
| [InstallmentNumber](Crm.Sales.SalesOrderPaymentPlans.md#installmentnumber) | int32 | Consequtive installment number. Used for identifying different payments generated according this payment plan. [Required] 
| [Notes](Crm.Sales.SalesOrderPaymentPlans.md#notes) | string (nullable) | Notes for this SalesOrderPaymentPlan. 
| [PaymentStartDays](Crm.Sales.SalesOrderPaymentPlans.md#paymentstartdays) | int32 | Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method. [Required] [Default(0)] 
| [PaymentTermDays](Crm.Sales.SalesOrderPaymentPlans.md#paymenttermdays) | int32 | Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. [Required] [Default(0)] 
| [Remainder](Crm.Sales.SalesOrderPaymentPlans.md#remainder) | boolean | Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount). [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PaymentAccount](Crm.Sales.SalesOrderPaymentPlans.md#paymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | Specifies the payment account towards which the payment is expected. null means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred. [Filter(multi eq)] |
| [PaymentType](Crm.Sales.SalesOrderPaymentPlans.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Specifies the expected payment type. null means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred. [Filter(multi eq)] |
| [SalesOrder](Crm.Sales.SalesOrderPaymentPlans.md#salesorder) | [SalesOrders](Crm.Sales.SalesOrders.md) | The [SalesOrder](Crm.Sales.SalesOrderPaymentPlans.md#salesorder) to which this SalesOrderPaymentPlan belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Amount

Amount to be payed. [Currency: SalesOrder.DocumentCurrency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AmountPercent

Percent of the sales order amount to be payed.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DueDateFormMethod

Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. [Required]

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

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DueDateFormMethod, Int32) != 0), null, obj.ExplicitPaymentDueDate)`
### ExplicitPaymentDueStartDate

Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DueDateFormMethod, Int32) != 0), null, obj.ExplicitPaymentDueStartDate)`
### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InstallmentNumber

Consequtive installment number. Used for identifying different payments generated according this payment plan. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.SalesOrder.PaymentPlans.Select( c => c.InstallmentNumber).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.SalesOrder.PaymentPlans.Select( c => c.InstallmentNumber).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this SalesOrderPaymentPlan.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentStartDays

Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### PaymentTermDays

Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`IIF( ( ( Convert( obj.DueDateFormMethod, Int32) == 3) OrElse ( Convert( obj.DueDateFormMethod, Int32) == 4)), 0, obj.PaymentTermDays)`

_Front-End Recalc Expressions:_  
`IIF( ( ( Convert( obj.DueDateFormMethod, Int32) == 3) OrElse ( Convert( obj.DueDateFormMethod, Int32) == 4)), 0, obj.PaymentTermDays)`
### Remainder

Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount). [Required] [Default(false)]

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

Specifies the payment account towards which the payment is expected. null means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred. [Filter(multi eq)]

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesOrder.PaymentAccount`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.PaymentAccount.IfNullThen( obj.PaymentType.DefaultPaymentAccount.IfNullThen( obj.PaymentAccount))`
`obj.SalesOrder.PaymentAccount`
### PaymentType

Specifies the expected payment type. null means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesOrder.PaymentType`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.PaymentType`
### SalesOrder

The [SalesOrder](Crm.Sales.SalesOrderPaymentPlans.md#salesorder) to which this SalesOrderPaymentPlan belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[SalesOrders](Crm.Sales.SalesOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPaymentPlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPaymentPlans erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrderPaymentPlans erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrderPaymentPlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrderPaymentPlans?$top=10>

