# Table Crm_Invoices

Invoices issued by the enterprise companies. Entity: Crm_Invoices

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Id](#customer_id)|`uniqueidentifier` |The customer to which the invoice is issued|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document is issued. All amounts are in this currency|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the invoice|
|[Payment_Type_Description](#payment_type_description)|`nvarchar(20)` `ML`|Description of the payment type. Initially copied from the name of the Payment Type|
|[Delivery_Date](#delivery_date)|`datetime` |Date, when the delivery was effected. When NULL = document date|
|[Notes](#notes)|`nvarchar(254)` ||
|[Credit_Note_Original_Invoice_Id](#credit_note_original_invoice_id)|`uniqueidentifier` |When this is credit note, may contain the original Invoice. NULL for normal invoices or when the original document is unknown.|
|[Credit_Note_Description](#credit_note_description)|`nvarchar(254)` |Descriptions/reason for the credit note.|
|[Invoice_Id](#invoice_id)|`uniqueidentifier` `PK`||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Payment_Due_Start_Date](#payment_due_start_date)|`datetime` ||
|[VAT_Cash_Reporting_Mode](#vat_cash_reporting_mode)|`bit` |When true, specifies, that the special cash reporting mode should be used for VAT reporting. When false, the normal (classic) VAT reporting is used.|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |VAT deal type for this invoice. If deal type in entered then VAT entry is created for this deal type.|
|[IsValid](#isvalid)|`bit` |Used for internal purposes. 1 when the invoice is valid (released and not void) for summing|
|[VAT_Notes](#vat_notes)|`nvarchar(254)` |Description of the operation that will be entered in the VAT ledgers.|
|[Apply_Date](#apply_date)|`date` |When not NULL specifies that the VAT entry for this invoice should be applied for a different period than that specified by the document date.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Payment_Due_Date](#payment_due_date)|`datetime` |When not NULL specifies due date for the payment|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Automatic_Order_Linking](#automatic_order_linking)|`bit` |Specifies whether to automatically set Lines.Invoice_Order_Line_Id by searching invoice orders upon first release|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Description

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Credit_Note_Original_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Payment_Due_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### VAT_Cash_Reporting_Mode

| Property | Value |
| - | - |
|Type|bit|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### IsValid

| Property | Value |
| - | - |
|Type|bit|

### VAT_Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Automatic_Order_Linking

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


