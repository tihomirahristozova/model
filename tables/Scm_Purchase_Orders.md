# Table Scm_Purchase_Orders

Contains purchase order headers. The purchase orders are documents, sent to a supplier, to inform him for an order of goods or services. Entity: Scm_Purchase_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the products.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store in which the goods are expected to be received.|
|[Planned_Release_Date](#planned_release_date)|`datetime` |The date, when the document is planned to be realeased and send to the supplier.|
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` |When not null, specifies the planned delivery date for all lines.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for paying the order. NULL means to use the default, which is the document date.|
|[Invoice_Document_No](#invoice_document_no)|`nvarchar(20)` |Contains the purchase invoice number when it is known in advance, null otherwise.|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|

## Columns

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


