# Procedure Crm_Invoices_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoice_Id](#invoice_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` |The customer to which the invoice is issued|
|[Customer_Id_Text](#customer_id_text)|`nvarchar` `ML`|The name of the party|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document is issued. All amounts are in this currency|
|[Document_Currency_Id_Text](#document_currency_id_text)|`nvarchar` ||
|[Document_Currency_Sign](#document_currency_sign)|`nvarchar` |The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the invoice|
|[Payment_Type_Name](#payment_type_name)|`nvarchar` `ML`||
|[Payment_Type_Description](#payment_type_description)|`nvarchar` `ML`|Description of the payment type. Initially copied from the name of the Payment Type|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |VAT deal type for this invoice. If deal type in entered then VAT entry is created for this deal type.|
|[Apply_Date](#apply_date)|`date` |When not NULL specifies that the VAT entry for this invoice should be applied for a different period than that specified by the document date.|
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Notes](#notes)|`nvarchar` ||
|[VAT_Notes](#vat_notes)|`nvarchar` |Description of the operation that will be entered in the VAT ledgers.|
|[Credit_Note_Original_Invoice_Id](#credit_note_original_invoice_id)|`uniqueidentifier` |When this is credit note, may contain the original Invoice. NULL for normal invoices or when the original document is unknown.|
|[Credit_Note_Original_Invoice_Id_Text](#credit_note_original_invoice_id_text)|`nvarchar` ||
|[Credit_Note_Description](#credit_note_description)|`nvarchar` |Descriptions/reason for the credit note.|
|[Delivery_Date](#delivery_date)|`datetime` |Date, when the delivery was effected. When NULL = document date|
|[Total_Amount_Words](#total_amount_words)|`nvarchar` ||
|[Credit_Note_Original_Invoice_Document_No](#credit_note_original_invoice_document_no)|`nvarchar` ||
|[Credit_Note_Original_Invoice_Document_Date](#credit_note_original_invoice_document_date)|`datetime` ||
|[Lines_Total](#lines_total)|`decimal(0, 0)` ||
|[Amount_To_Pay](#amount_to_pay)|`decimal(0, 0)` ||
|[Lines_Total_Base_Currency](#lines_total_base_currency)|`decimal(0, 0)` ||
|[Amount_To_Pay_Base_Currency](#amount_to_pay_base_currency)|`decimal(0, 0)` ||

## Columns

### Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### VAT_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Credit_Note_Original_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Original_Invoice_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Credit_Note_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Total_Amount_Words

| Property | Value |
| - | - |
|Type|nvarchar|

### Credit_Note_Original_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Credit_Note_Original_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Lines_Total

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Amount_To_Pay

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lines_Total_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Amount_To_Pay_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


