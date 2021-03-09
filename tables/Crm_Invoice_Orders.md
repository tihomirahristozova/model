# Table Crm_Invoice_Orders

Invoice Orders can be created by different modules and order the creation of Invoices. Entity: Crm_Invoice_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoice_Order_Id](#invoice_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` |The primary customer to whom to invoice|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document is issued. All amounts are in this currency|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the invoice|
|[Payment_Type_Description](#payment_type_description)|`nvarchar(20)` |Description of the payment type. Initially copied from the name of the Payment Type|
|[Delivery_Date](#delivery_date)|`datetime` |Date, when the delivery was effected. When NULL = document date|
|[Notes](#notes)|`nvarchar(254)` ||
|[Credit_Note_Original_Invoice_Id](#credit_note_original_invoice_id)|`uniqueidentifier` |When the order is for credit note, may contain the original Invoice. NULL for normal orders or when the original document is unknown.|
|[Credit_Note_Description](#credit_note_description)|`nvarchar(254)` |Descriptions/reason for the credit note.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Payment_Due_Start_Date](#payment_due_start_date)|`datetime` |The date when the payment becomes due for documents with one installment.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |Default value and filter for the lines. Used to differenciate the invoice order for each sales order.|
|[Credit_Note_Original_Invoice_Order_Id](#credit_note_original_invoice_order_id)|`uniqueidentifier` |When the invoice is a credit note, can specify the original Invoice Order, on which this is based. NULL for normal invoice orders or when the original document is unknown.|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |VAT deal type for this invoice order. This deal type is copied to the invoice to create VAT entries.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Payment_Due_Date](#payment_due_date)|`datetime` |When not NULL specifies due date for the payment|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|
|[Apply_Date](#apply_date)|`datetime` |Apply date to be passed to the invoice. When not NULL specifies that the VAT entry should be applied for a different period than that specified by the document date.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Invoice_Order_Id

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

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Payment_Due_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Original_Invoice_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


