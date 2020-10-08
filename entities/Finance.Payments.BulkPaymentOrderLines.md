---
uid: Finance.Payments.BulkPaymentOrderLines
---
# Finance.Payments.BulkPaymentOrderLines

Bulk payment order document line. Each line usually creates one payment order. Entity: Cash_Bulk_Payment_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Payments.BulkPaymentOrderLines.md#Id) | guid |  
| [BillTo](Finance.Payments.BulkPaymentOrderLines.md#BillTo) | [Finance.Payments.BulkPaymentOrderLinesRepository.BillTo](Finance.Payments.BulkPaymentOrderLines.md#BillTo) (nullable) | If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. 
| [Direction](Finance.Payments.BulkPaymentOrderLines.md#Direction) | [Finance.Payments.BulkPaymentOrderLinesRepository.Direction](Finance.Payments.BulkPaymentOrderLines.md#Direction) | I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)] 
| [DueDate](Finance.Payments.BulkPaymentOrderLines.md#DueDate) | datetime (nullable) | The due date of the payment. null means there is no due date. [Filter(ge;le)] 
| [InstallmentNumber](Finance.Payments.BulkPaymentOrderLines.md#InstallmentNumber) | int32 (nullable) | Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. 
| [InvoiceAmount](Finance.Payments.BulkPaymentOrderLines.md#InvoiceAmount) | [Amount](../data-types.md#Amount) (nullable) | The specified invoice amount. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency] 
| [IsAmountWithVAT](Finance.Payments.BulkPaymentOrderLines.md#IsAmountWithVAT) | boolean | Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Finance.Payments.BulkPaymentOrderLines.md#Notes) | string (nullable) | Notes for this BulkPaymentOrderLine. 
| [RefDocumentDate](Finance.Payments.BulkPaymentOrderLines.md#RefDocumentDate) | datetime (nullable) | The date of the base document. null means that it is unknown. 
| [RefDocumentNo](Finance.Payments.BulkPaymentOrderLines.md#RefDocumentNo) | string | The number of the document which is the basis for the payment. [Required] 
| [RefInvoiceApplyDate](Finance.Payments.BulkPaymentOrderLines.md#RefInvoiceApplyDate) | datetime (nullable) | The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. 
| [RefInvoiceDocumentDate](Finance.Payments.BulkPaymentOrderLines.md#RefInvoiceDocumentDate) | datetime (nullable) | The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. 
| [RefInvoiceDocumentNo](Finance.Payments.BulkPaymentOrderLines.md#RefInvoiceDocumentNo) | string (nullable) | The number of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. 
| [TotalAmount](Finance.Payments.BulkPaymentOrderLines.md#TotalAmount) | [Amount](../data-types.md#Amount) | Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#BulkPaymentOrder) | [Finance.Payments.BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md) | The [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#BulkPaymentOrder) to which this BulkPaymentOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [InvoiceAmountCurrency](Finance.Payments.BulkPaymentOrderLines.md#InvoiceAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency of Invoice Amount. [Filter(multi eq)] |
| [LocationParty](Finance.Payments.BulkPaymentOrderLines.md#LocationParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Location or sub-party of the Party_Id. [Filter(multi eq)] |
| [Party](Finance.Payments.BulkPaymentOrderLines.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which is to pay or receive the amount. [Required] [Filter(multi eq)] |
| [PaymentAccount](Finance.Payments.BulkPaymentOrderLines.md#PaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.BulkPaymentOrderLines.md#PaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Expected payment type. When null, there is no expectation for payment type. [Filter(multi eq)] |
| [RefDocumentType](Finance.Payments.BulkPaymentOrderLines.md#RefDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The type of the document which is the basis for the payment. [Required] [Filter(multi eq)] |
| [RefInvoiceDocumentType](Finance.Payments.BulkPaymentOrderLines.md#RefInvoiceDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | The document type of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)] |
| [TotalAmountCurrency](Finance.Payments.BulkPaymentOrderLines.md#TotalAmountCurrency) | [General.Currencies](General.Currencies.md) | The currency of Total Amount. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BillTo

> If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified.

_Type_: **[Finance.Payments.BulkPaymentOrderLinesRepository.BillTo](Finance.Payments.BulkPaymentOrderLines.md#BillTo) (nullable)**  
Allowed values for the [BillTo](Finance.Payments.BulkPaymentOrderLines.md#BillTo) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Direction

> I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)]

_Type_: **[Finance.Payments.BulkPaymentOrderLinesRepository.Direction](Finance.Payments.BulkPaymentOrderLines.md#Direction)**  
Allowed values for the [Direction](Finance.Payments.BulkPaymentOrderLines.md#Direction) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Expense**  

### DueDate

> The due date of the payment. null means there is no due date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### InstallmentNumber

> Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InvoiceAmount

> The specified invoice amount. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsAmountWithVAT

> Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this BulkPaymentOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentDate

> The date of the base document. null means that it is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentNo

> The number of the document which is the basis for the payment. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceApplyDate

> The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceDocumentDate

> The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceDocumentNo

> The number of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TotalAmount

> Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### BulkPaymentOrder

> The [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#BulkPaymentOrder) to which this BulkPaymentOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Payments.BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### InvoiceAmountCurrency

> The currency of Invoice Amount. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LocationParty

> Location or sub-party of the Party_Id. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The party which is to pay or receive the amount. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.LocationParty.ParentParty`
### PaymentAccount

> When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.PaymentType.GetDefaultPaymentAccount().IfNullThen(obj.PaymentAccount)`
### PaymentType

> Expected payment type. When null, there is no expectation for payment type. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefDocumentType

> The type of the document which is the basis for the payment. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefInvoiceDocumentType

> The document type of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TotalAmountCurrency

> The currency of Total Amount. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.PaymentAccount.Currency`


## Business Rules

[!list erp.entity=Finance.Payments.BulkPaymentOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.BulkPaymentOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.BulkPaymentOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_BulkPaymentOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_BulkPaymentOrderLines?$top=10>

