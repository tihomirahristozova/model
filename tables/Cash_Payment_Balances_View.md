# View Cash_Payment_Balances_View

Represents the payment orders with their covered amounts. Entity: Cash_Payment_Balances_View

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
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of amounts.|
|[Paid_Amount](#paid_amount)|`decimal(38, 2)` |The paid amount. Taken from released payment transactions.|
|[Order_Amount](#order_amount)|`decimal(18, 2)` |The total amount of the payment order.|
|[Due_Start_Date](#due_start_date)|`date` |The date at which the payment becomes executable. NULL means the payment is executable at all times.|
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` |Location or sub-party of the Party_Id in the order|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Is_Invoiced](#is_invoiced)|`bit` |When Is_Invoiced = true, then in the view results will be included only the Payment Orders which do have a RefInvoiceDocument. If Is_Invoiced = false, then in the view results will be included only the Payment Orders which do NOT have a RefInvoiceDocument.|

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

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Paid_Amount

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Order_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Invoiced

| Property | Value |
| - | - |
|Type|bit|


