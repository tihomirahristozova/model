# Procedure Scm_Receiving_Orders_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` `PK`||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order which is received with this receiving order.|
|[Purchase_Order_Id_Text](#purchase_order_id_text)|`nvarchar` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the products for this receiving order.|
|[Supplier_Id_Text](#supplier_id_text)|`nvarchar` ||
|[Store_Id](#store_id)|`uniqueidentifier` |The store in which the goods were received.|
|[Store_Id_Text](#store_id_text)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Document_Currency_Id_Text](#document_currency_id_text)|`nvarchar` ||
|[Planned_Release_Date](#planned_release_date)|`datetime` |The date, when the document is planned to be realeased.|
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` |When not null, specifies the planned delivery date for all lines.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for the payment. When null, the payment due date is the documents date.|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.|

## Columns

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

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

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


