---
uid: Finance.Payments.OrderBalances
---
# Finance.Payments.OrderBalances

Represents the payment orders with their covered amounts. Entity: Cash_Payment_Balances_View

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Direction](Finance.Payments.OrderBalances.md#Direction) | [Finance.Payments.PaymentOrdersRepository.Direction](Finance.Payments.OrderBalances.md#Direction) | I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)] 
| [DueDate](Finance.Payments.OrderBalances.md#DueDate) | datetime (nullable) | The due date of the payment. null means there is no due date. [Filter(eq;ge;le)] 
| [DueStartDate](Finance.Payments.OrderBalances.md#DueStartDate) | date (nullable) | The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)] 
| [IsInvoiced](Finance.Payments.OrderBalances.md#IsInvoiced) | boolean | When Is_Invoiced = true, then in the view results will be included only the Payment Orders which do have a RefInvoiceDocument. If Is_Invoiced = false, then in the view results will be included only the Payment Orders which do NOT have a RefInvoiceDocument. [Required] [Filter(multi eq)] 
| [OrderAmount](Finance.Payments.OrderBalances.md#OrderAmount) | [Amount](../data-types.md#Amount) | The total amount of the payment order. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)] 
| [PaidAmount](Finance.Payments.OrderBalances.md#PaidAmount) | [Amount](../data-types.md#Amount) | The paid amount. Taken from released payment transactions. [Currency: Currency] [Required] 
| [RefDocumentDate](Finance.Payments.OrderBalances.md#RefDocumentDate) | datetime (nullable) | The date of the original document. null means that it is unknown. [Filter(eq)] 
| [RefDocumentNo](Finance.Payments.OrderBalances.md#RefDocumentNo) | string | The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)] 
| [RefInvoiceDocumentDate](Finance.Payments.OrderBalances.md#RefInvoiceDocumentDate) | datetime (nullable) | The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)] 
| [RefInvoiceDocumentNo](Finance.Payments.OrderBalances.md#RefInvoiceDocumentNo) | string (nullable) | The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Payments.OrderBalances.md#Currency) | [General.Currencies](General.Currencies.md) | The currency of amounts. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Finance.Payments.OrderBalances.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [LocationParty](Finance.Payments.OrderBalances.md#LocationParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Location or sub-party of the Party_Id in the order. [Filter(multi eq)] |
| [Party](Finance.Payments.OrderBalances.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which is to pay or receive the amount. [Required] [Filter(multi eq)] |
| [PaymentOrder](Finance.Payments.OrderBalances.md#PaymentOrder) | [Finance.Payments.PaymentOrders](Finance.Payments.PaymentOrders.md) | The payment order. [Required] [Default(New Guid)] [Filter(multi eq)] |
| [RefDocument](Finance.Payments.OrderBalances.md#RefDocument) | [General.Documents](General.Documents.md) (nullable) | The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)] |
| [RefDocumentType](Finance.Payments.OrderBalances.md#RefDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)] |
| [RefInvoiceDocument](Finance.Payments.OrderBalances.md#RefInvoiceDocument) | [General.Documents](General.Documents.md) (nullable) | The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)] |
| [RefInvoiceDocumentType](Finance.Payments.OrderBalances.md#RefInvoiceDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)] |


## Attribute Details

### Direction

> I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)]

_Type_: **[Finance.Payments.PaymentOrdersRepository.Direction](Finance.Payments.OrderBalances.md#Direction)**  
Allowed values for the [Direction](Finance.Payments.PaymentOrders.md#Direction) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Expense**  

### DueDate

> The due date of the payment. null means there is no due date. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DueStartDate

> The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IsInvoiced

> When Is_Invoiced = true, then in the view results will be included only the Payment Orders which do have a RefInvoiceDocument. If Is_Invoiced = false, then in the view results will be included only the Payment Orders which do NOT have a RefInvoiceDocument. [Required] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OrderAmount

> The total amount of the payment order. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PaidAmount

> The paid amount. Taken from released payment transactions. [Currency: Currency] [Required]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentDate

> The date of the original document. null means that it is unknown. [Filter(eq)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentDate`
### RefDocumentNo

> The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentNo`
### RefInvoiceDocumentDate

> The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentDate`
### RefInvoiceDocumentNo

> The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentNo`

## Reference Details

### Currency

> The currency of amounts. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The enterprise company which issued the document. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LocationParty

> Location or sub-party of the Party_Id in the order. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The party which is to pay or receive the amount. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PaymentOrder

> The payment order. [Required] [Default(New Guid)] [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentOrders](Finance.Payments.PaymentOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### RefDocument

> The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefDocumentType

> The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentType`
### RefInvoiceDocument

> The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefInvoiceDocumentType

> The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentType`


## Business Rules

[!list erp.entity=Finance.Payments.OrderBalances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.OrderBalances erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.OrderBalances erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_OrderBalances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_OrderBalances?$top=10>

