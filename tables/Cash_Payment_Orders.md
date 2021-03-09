# Table Cash_Payment_Orders

Each payment order contains a receivable or payable amount. Entity: Cash_Payment_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Ref_Document_Id](#ref_document_id)|`uniqueidentifier` |The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document.|
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` |The type of the document which has created the payment order and is the basis for the payment|
|[Ref_Document_No](#ref_document_no)|`nvarchar(20)` |The number of the document which has created the payment order and is the basis for the payment|
|[Ref_Document_Date](#ref_document_date)|`datetime` |The date of the original document. NULL means that it is unknown|
|[Ref_Invoice_Document_Id](#ref_invoice_document_id)|`uniqueidentifier` |The invoice document which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document.|
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` |The document type of the invoice which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar(20)` |The number of the invoice which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` |The date of the related invoice. NULL means that the payment order isn't related to any invoice or the date is unknown.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party which is to pay or receive the amount|
|[Due_Date](#due_date)|`datetime` |The due date of the payment. NULL means there is no due date|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |Total amount that should be payed|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of Total Amount.|
|[Invoice_Amount](#invoice_amount)|`decimal(18, 2)` |The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount)|
|[Invoice_Amount_Currency_Id](#invoice_amount_currency_id)|`uniqueidentifier` |The currency of Invoice Amount|
|[Notes](#notes)|`nvarchar(254)` ||
|[Due_Start_Date](#due_start_date)|`date` |The date at which the payment becomes executable. NULL means the payment is executable at all times.|
|[Allow_Close_Not_Paid](#allow_close_not_paid)|`bit` |1 to allow closing of payment orders, that are not fully paid|
|[Ref_Invoice_Apply_Date](#ref_invoice_apply_date)|`datetime` |The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Expected payment type. Null when there is no expectation. Can also specify default payment account.|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` `PK`||
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` |Location or sub-party of the Party_Id in the order|
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` |Is_Amount_With_VAT=1 if the requested amount includes VAT|
|[Row_Version](#row_version)|`timestamp` ||
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying the payment when using payment plans. NULL means that the payment is not part of a payment plan|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the payment account that is expected or will be used by the payment transaction|
|[Document_Id](#document_id)|`uniqueidentifier` |The document data of the payment order itself|
|[Bill_To](#bill_to)|`nvarchar(1)` Allowed: `C`, `L`|If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), NULL = unidentified|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |When not NULL, contains suggested fiscal printer for printing fiscal notes upon payment.|

## Columns

### Ref_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Document_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Ref_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Ref_Invoice_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Invoice_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Ref_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Invoice_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Allow_Close_Not_Paid

| Property | Value |
| - | - |
|Type|bit|

### Ref_Invoice_Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Amount_With_VAT

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


