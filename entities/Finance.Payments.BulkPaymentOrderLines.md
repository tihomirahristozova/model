---
uid: Finance.Payments.BulkPaymentOrderLines
---
# Finance.Payments.BulkPaymentOrderLines Entity

**Namespace:** [Finance.Payments](Finance.Payments.md)  

Bulk payment order document line. Each line usually creates one payment order. Entity: Cash_Bulk_Payment_Order_Lines

## Default Visualization
Default Display Text Format:  
_{BulkPaymentOrder.DocumentType.Code}:{BulkPaymentOrder.DocumentNo} - {BulkPaymentOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_BulkPaymentOrder.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Payments.BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md)  
Aggregate Root:  
[Finance.Payments.BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BillTo](Finance.Payments.BulkPaymentOrderLines.md#billto) | [BillTo](Finance.Payments.BulkPaymentOrderLines.md#billto) (nullable) | If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. 
| [Direction](Finance.Payments.BulkPaymentOrderLines.md#direction) | [Direction](Finance.Payments.BulkPaymentOrderLines.md#direction) | I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)] 
| [DueDate](Finance.Payments.BulkPaymentOrderLines.md#duedate) | datetime (nullable) | The due date of the payment. null means there is no due date. [Filter(ge;le)] 
| [Id](Finance.Payments.BulkPaymentOrderLines.md#id) | guid |  
| [InstallmentNumber](Finance.Payments.BulkPaymentOrderLines.md#installmentnumber) | int32 (nullable) | Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. 
| [InvoiceAmount](Finance.Payments.BulkPaymentOrderLines.md#invoiceamount) | [Amount](../data-types.md#amount) (nullable) | The specified invoice amount. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency] 
| [IsAmountWithVAT](Finance.Payments.BulkPaymentOrderLines.md#isamountwithvat) | boolean | Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Finance.Payments.BulkPaymentOrderLines.md#notes) | string (nullable) | Notes for this BulkPaymentOrderLine. 
| [RefDocumentDate](Finance.Payments.BulkPaymentOrderLines.md#refdocumentdate) | datetime (nullable) | The date of the base document. null means that it is unknown. 
| [RefDocumentNo](Finance.Payments.BulkPaymentOrderLines.md#refdocumentno) | string | The number of the document which is the basis for the payment. [Required] 
| [RefInvoiceApplyDate](Finance.Payments.BulkPaymentOrderLines.md#refinvoiceapplydate) | datetime (nullable) | The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. 
| [RefInvoiceDocumentDate](Finance.Payments.BulkPaymentOrderLines.md#refinvoicedocumentdate) | datetime (nullable) | The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. 
| [RefInvoiceDocumentNo](Finance.Payments.BulkPaymentOrderLines.md#refinvoicedocumentno) | string (nullable) | The number of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. 
| [TotalAmount](Finance.Payments.BulkPaymentOrderLines.md#totalamount) | [Amount](../data-types.md#amount) | Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#bulkpaymentorder) | [BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md) | The [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#bulkpaymentorder) to which this BulkPaymentOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [InvoiceAmountCurrency](Finance.Payments.BulkPaymentOrderLines.md#invoiceamountcurrency) | [Currencies](General.Currencies.md) (nullable) | The currency of Invoice Amount. [Filter(multi eq)] |
| [LocationParty](Finance.Payments.BulkPaymentOrderLines.md#locationparty) | [Parties](General.Contacts.Parties.md) (nullable) | Location or sub-party of the Party_Id. [Filter(multi eq)] |
| [Party](Finance.Payments.BulkPaymentOrderLines.md#party) | [Parties](General.Contacts.Parties.md) | The party which is to pay or receive the amount. [Required] [Filter(multi eq)] |
| [PaymentAccount](Finance.Payments.BulkPaymentOrderLines.md#paymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.BulkPaymentOrderLines.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Expected payment type. When null, there is no expectation for payment type. [Filter(multi eq)] |
| [RefDocumentType](Finance.Payments.BulkPaymentOrderLines.md#refdocumenttype) | [DocumentTypes](General.DocumentTypes.md) | The type of the document which is the basis for the payment. [Required] [Filter(multi eq)] |
| [RefInvoiceDocumentType](Finance.Payments.BulkPaymentOrderLines.md#refinvoicedocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | The document type of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)] |
| [TotalAmountCurrency](Finance.Payments.BulkPaymentOrderLines.md#totalamountcurrency) | [Currencies](General.Currencies.md) | The currency of Total Amount. [Required] [Filter(multi eq)] |


## Attribute Details

### BillTo

If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified.

_Type_: **[BillTo](Finance.Payments.BulkPaymentOrderLines.md#billto) (nullable)**  
Allowed values for the [BillTo](Finance.Payments.BulkPaymentOrderLines.md#billto) data attribute  
_Allowed Values (Finance.Payments.BulkPaymentOrderLinesRepository.BillTo Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Direction

I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)]

_Type_: **[Direction](Finance.Payments.BulkPaymentOrderLines.md#direction)**  
Allowed values for the [Direction](Finance.Payments.BulkPaymentOrderLines.md#direction) data attribute  
_Allowed Values (Finance.Payments.BulkPaymentOrderLinesRepository.Direction Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Expense**  

### DueDate

The due date of the payment. null means there is no due date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InstallmentNumber

Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InvoiceAmount

The specified invoice amount. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsAmountWithVAT

Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this BulkPaymentOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentDate

The date of the base document. null means that it is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentNo

The number of the document which is the basis for the payment. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceApplyDate

The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceDocumentDate

The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefInvoiceDocumentNo

The number of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TotalAmount

Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### BulkPaymentOrder

The [BulkPaymentOrder](Finance.Payments.BulkPaymentOrderLines.md#bulkpaymentorder) to which this BulkPaymentOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[BulkPaymentOrders](Finance.Payments.BulkPaymentOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### InvoiceAmountCurrency

The currency of Invoice Amount. [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### LocationParty

Location or sub-party of the Party_Id. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party which is to pay or receive the amount. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.LocationParty.ParentParty`
### PaymentAccount

When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)]

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.PaymentType.GetDefaultPaymentAccount( ).IfNullThen( obj.PaymentAccount)`
### PaymentType

Expected payment type. When null, there is no expectation for payment type. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### RefDocumentType

The type of the document which is the basis for the payment. [Required] [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RefInvoiceDocumentType

The document type of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TotalAmountCurrency

The currency of Total Amount. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.PaymentAccount.Currency`


## Business Rules

[!list erp.entity=Finance.Payments.BulkPaymentOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.BulkPaymentOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_BulkPaymentOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_BulkPaymentOrderLines?$top=10>

