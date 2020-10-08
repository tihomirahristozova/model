---
uid: Crm.Sales.DefaultSalesOrderPaymentPlans
---
# Crm.Sales.DefaultSalesOrderPaymentPlans

Default payment plan for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Payment_Plans

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.DefaultSalesOrderPaymentPlans.md#Id) | guid |  
| [AmountPercent](Crm.Sales.DefaultSalesOrderPaymentPlans.md#AmountPercent) | decimal (nullable) | Percent of the sales order amount to be payed. 
| [DueDateFormMethod](Crm.Sales.DefaultSalesOrderPaymentPlans.md#DueDateFormMethod) | [Crm.PaymentPlanDueDateSource](Crm.Sales.DefaultSalesOrderPaymentPlans.md#DueDateFormMethod) | Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. [Required] 
| [InstallmentNumber](Crm.Sales.DefaultSalesOrderPaymentPlans.md#InstallmentNumber) | int32 | Consequtive installment number. Used for identifying different payments generated according this payment plan. [Required] 
| [PaymentTermDays](Crm.Sales.DefaultSalesOrderPaymentPlans.md#PaymentTermDays) | int32 | Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. [Required] [Default(0)] 
| [Remainder](Crm.Sales.DefaultSalesOrderPaymentPlans.md#Remainder) | boolean | Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent). [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](Crm.Sales.DefaultSalesOrderPaymentPlans.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The [DocumentType](General.DocumentTypes.md) to which this DefaultSalesOrderPaymentPlan belongs. [Required] [Filter(multi eq)] [Owner] |
| [EnterpriseCompany](Crm.Sales.DefaultSalesOrderPaymentPlans.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | Enterprise company for which the current default installment template is valid. If enterprise company is not set then the installment template is valid for all enterprise companies. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.Sales.DefaultSalesOrderPaymentPlans.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | Enterprise company location (within the chosen enterprise company) for which the current default installment template is valid. If enterprise company location is not set then the installment template is valid for all enterprise company locations. [Filter(multi eq)] |
| [PaymentAccount](Crm.Sales.DefaultSalesOrderPaymentPlans.md#PaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | Default payment account for the current installment. null means that there is no default account. [Filter(multi eq)] |
| [PaymentType](Crm.Sales.DefaultSalesOrderPaymentPlans.md#PaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Default payment type for the current installment. null means that there is no default payment type. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AmountPercent

> Percent of the sales order amount to be payed.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DueDateFormMethod

> Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. [Required]

_Type_: **[Crm.PaymentPlanDueDateSource](Crm.Sales.DefaultSalesOrderPaymentPlans.md#DueDateFormMethod)**  
Generic enum type for PaymentPlanDueDateSource properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| SpecifyTheDateExplicitly | SpecifyTheDateExplicitly value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SpecifyTheDateExplicitly' |
| UseInvoiceDate | UseInvoiceDate value. Stored as 'INV'. <br /> _Database Value:_ 'INV' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'UseInvoiceDate' |
| UseSalesOrderDate | UseSalesOrderDate value. Stored as 'SLS'. <br /> _Database Value:_ 'SLS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'UseSalesOrderDate' |
| UseSalesOrderDueDate | UseSalesOrderDueDate value. Stored as 'SDD'. <br /> _Database Value:_ 'SDD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'UseSalesOrderDueDate' |
| UseInvoiceDueDate | UseInvoiceDueDate value. Stored as 'IDD'. <br /> _Database Value:_ 'IDD' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'UseInvoiceDueDate' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InstallmentNumber

> Consequtive installment number. Used for identifying different payments generated according this payment plan. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.DocumentType.DefaultSalesOrderPaymentPlans.Select(c => c.InstallmentNumber).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.DocumentType.DefaultSalesOrderPaymentPlans.Select(c => c.InstallmentNumber).DefaultIfEmpty(0).Max() + 10)`
### PaymentTermDays

> Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Remainder

> Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent). [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DocumentType

> The [DocumentType](General.DocumentTypes.md) to which this DefaultSalesOrderPaymentPlan belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> Enterprise company for which the current default installment template is valid. If enterprise company is not set then the installment template is valid for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> Enterprise company location (within the chosen enterprise company) for which the current default installment template is valid. If enterprise company location is not set then the installment template is valid for all enterprise company locations. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PaymentAccount

> Default payment account for the current installment. null means that there is no default account. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PaymentType

> Default payment type for the current installment. null means that there is no default payment type. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Sales.DefaultSalesOrderPaymentPlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.DefaultSalesOrderPaymentPlans erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.DefaultSalesOrderPaymentPlans erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_DefaultSalesOrderPaymentPlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_DefaultSalesOrderPaymentPlans?$top=10>

