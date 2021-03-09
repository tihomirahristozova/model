# Table Crm_Invoice_Order_Lines

Detail records (lines) of Invoice Orders. Entity: Crm_Invoice_Order_Lines

## Owner Tables Hierarchy

* [Crm_Invoice_Orders](Crm_Invoice_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoice_Order_Line_Id](#invoice_order_line_id)|`uniqueidentifier` `PK`||
|[Invoice_Order_Id](#invoice_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is ordered for invoicing|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The description of Product. Initially copied from the name of the Product or from the generating document.|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity of the product to invoice|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |Unit selling price in the unit of measure, specified in Quantity Unit|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |User-defined discount for the line|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |The line discount type used to form the Line_Standard_Discount_Percent|
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` |Standard discount for the line. This is automatically computed according to discount conditions|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` |The store transaction line that is to be invoiced by this line, for Business Reason = S|
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` |The payment transaction, which is to be invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment.|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalent of Quantity in the base measurement unit of the Product|
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type to be passed to the invoice line. If deal type in the line is different from deal type in the header another VAT entry is created from the invoice.|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` |When not NULL specifies the Sales Order line that is ordered to be invoiced by this line|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |When not NULL specifies the Sales Order that is ordered to be invoiced by this line|
|[Business_Reason](#business_reason)|`nvarchar(1)` Allowed: `P`, `S`|Business reason for invoicing of this product or service. S=Shipment, P=Payment|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Invoice_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Business_Reason

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


