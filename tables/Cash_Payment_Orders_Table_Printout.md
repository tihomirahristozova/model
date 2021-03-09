# Procedure Cash_Payment_Orders_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Ref_Document_Id](#ref_document_id)|`uniqueidentifier` |The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document.|
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` |The type of the document which has created the payment order and is the basis for the payment|
|[Ref_Document_No](#ref_document_no)|`nvarchar` |The number of the document which has created the payment order and is the basis for the payment|
|[Ref_Document_Date](#ref_document_date)|`datetime` |The date of the original document. NULL means that it is unknown|
|[Ref_Invoice_Document_Id](#ref_invoice_document_id)|`uniqueidentifier` |The invoice document which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document.|
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` |The document type of the invoice which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar` |The number of the invoice which has created or is related to the payment order and is the basis for the payment. NULL means that the payment order isn't created or related to any invoice.|
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` |The date of the related invoice. NULL means that the payment order isn't related to any invoice or the date is unknown.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party which is to pay or receive the amount|
|[Due_Date](#due_date)|`datetime` |The due date of the payment. NULL means there is no due date|
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |Total amount that should be payed|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of Total Amount.|
|[Invoice_Amount](#invoice_amount)|`decimal(18, 2)` |The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount)|
|[Invoice_Amount_Currency_Id](#invoice_amount_currency_id)|`uniqueidentifier` |The currency of Invoice Amount|
|[Notes](#notes)|`nvarchar` ||
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying the payment when using payment plans. NULL means that the payment is not part of a payment plan|
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` |Is_Amount_With_VAT=1 if the requested amount includes VAT|
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` ||
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` `PK`||
|[Total_Amount_Currency_Name](#total_amount_currency_name)|`nvarchar` ||
|[Total_Amount_Currency_Sign](#total_amount_currency_sign)|`nvarchar` ||
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`||
|[Total_Amount_Words](#total_amount_words)|`nvarchar` ||
|[Ref_Document_Type_Name](#ref_document_type_name)|`nvarchar` ||
|[Party_Id_Text](#party_id_text)|`nvarchar` `ML`|The name of the party|
|[Document_Id](#document_id)|`uniqueidentifier` |The document data of the payment order itself|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the payment account that is expected or will be used by the payment transaction|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||

## Columns

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Is_Amount_With_VAT

| Property | Value |
| - | - |
|Type|bit|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Amount_Currency_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount_Words

| Property | Value |
| - | - |
|Type|nvarchar|

### Ref_Document_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


