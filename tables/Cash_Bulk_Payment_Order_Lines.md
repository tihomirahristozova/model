# Table Cash_Bulk_Payment_Order_Lines

Bulk payment order document line. Each line usually creates one payment order. Entity: Cash_Bulk_Payment_Order_Lines

## Owner Tables Hierarchy

* [Cash_Bulk_Payment_Orders](Cash_Bulk_Payment_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` |The type of the document which is the basis for the payment|
|[Ref_Document_No](#ref_document_no)|`nvarchar(20)` |The number of the document which is the basis for the payment|
|[Ref_Document_Date](#ref_document_date)|`datetime` |The date of the base document. NULL means that it is unknown|
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` |The document type of the invoice which is related and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar(20)` |The number of the invoice which is related and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` |The date of the related invoice. NULL means that the payment order isn't related to any invoice or the date is unknown.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party which is to pay or receive the amount|
|[Due_Date](#due_date)|`datetime` |The due date of the payment. NULL means there is no due date|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |Total amount that should be payed|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of Total Amount|
|[Invoice_Amount](#invoice_amount)|`decimal(18, 2)` |The specified invoice amount. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount)|
|[Invoice_Amount_Currency_Id](#invoice_amount_currency_id)|`uniqueidentifier` |The currency of Invoice Amount|
|[Notes](#notes)|`nvarchar(254)` ||
|[Bill_To](#bill_to)|`nvarchar(1)` Allowed: `C`, `L`|If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), NULL = unidentified|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Expected payment type. When null, there is no expectation for payment type.|
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` |Location or sub-party of the Party_Id|
|[Bulk_Payment_Order_Line_Id](#bulk_payment_order_line_id)|`uniqueidentifier` `PK`||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the payment account that is expected or will be used by the payment transaction|
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying the payment when using payment plans. NULL means that the payment is not part of a payment plan|
|[Ref_Invoice_Apply_Date](#ref_invoice_apply_date)|`datetime` |The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown.|
|[Bulk_Payment_Order_Id](#bulk_payment_order_id)|`uniqueidentifier` ||
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` |Is_Amount_With_VAT=1 if the requested amount includes VAT|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

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

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bulk_Payment_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Ref_Invoice_Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Bulk_Payment_Order_Id

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


