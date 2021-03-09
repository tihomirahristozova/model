# Table Scm_Receiving_Orders

Contains the received quantities from a supplier. Entity: Scm_Receiving_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` `PK`||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order which is received with this receiving order.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the products for this receiving order.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store in which the goods were received.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Planned_Release_Date](#planned_release_date)|`datetime` |The date, when the document is planned to be realeased.|
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` |When not null, specifies the planned delivery date for all lines.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for the payment. When null, the payment due date is the documents date.|
|[Invoice_Document_No](#invoice_document_no)|`nvarchar(20)` |Contains the purchase invoice number when it is known in advance, null otherwise.|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.|
|[Purchase_Lot_Description](#purchase_lot_description)|`nvarchar(254)` |Description of the purchase lot for the whole document. It is set for the lots created by this receiving order.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|

## Columns

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Document_Currency_Id

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

### Purchase_Lot_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

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


