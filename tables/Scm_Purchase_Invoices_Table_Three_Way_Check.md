# Procedure Scm_Purchase_Invoices_Table_Three_Way_Check


## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` ||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. NULL means that there is no linked RO and the 2 or 3 way check will not include the RO|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product.|
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Invoice_Quantity](#invoice_quantity)|`decimal(0, 0)` ||
|[Purchase_Quantity](#purchase_quantity)|`decimal(0, 0)` ||
|[Receiving_Quantity](#receiving_quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Purchase_Invoice_Amount](#purchase_invoice_amount)|`decimal(0, 0)` ||
|[Purchase_Invoice_Currency_Id](#purchase_invoice_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Purchase_Order_Amount](#purchase_order_amount)|`decimal(0, 0)` ||
|[Purchase_Order_Currency_Id](#purchase_order_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Receiving_Order_Amount](#receiving_order_amount)|`decimal(0, 0)` ||
|[Receiving_Order_Currency_Id](#receiving_order_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|

## Columns

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Invoice_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receiving_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Invoice_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Order_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receiving_Order_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


