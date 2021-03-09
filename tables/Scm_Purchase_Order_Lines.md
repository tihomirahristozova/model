# Table Scm_Purchase_Order_Lines

Contains detail lines of purchase orders. Entity: Scm_Purchase_Order_Lines

## Owner Tables Hierarchy

* [Scm_Purchase_Orders](Scm_Purchase_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The ordered product.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity ordered.|
|[Confirmed_Quantity](#confirmed_quantity)|`decimal(18, 3)` |The quantity that is confirmed by the supplier. NULL if there was no order confirmation.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Price_Per_Unit](#price_per_unit)|`decimal(14, 5)` |The expected unit price of the ordered products, in the document currency.|
|[Confirmed_Price_Per_Unit](#confirmed_price_per_unit)|`decimal(14, 5)` |The unit price that is confirmed by the supplier. NULL if there was no order confirmation.|
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` |The planned delivery date for this line.|
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` |When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |When not NULL, specifies that the product was selected using the specified product code record.|
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` |When not NULL, specifies that the current line is based on the specified requisition line.|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Quantity, in the base measurement category of the product.|
|[Confirmed_Quantity_Base](#confirmed_quantity_base)|`decimal(18, 3)` Readonly|The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |When not null, indicates that a specific lot is required to be delivered.|
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Line_No](#parent_line_no)|`int` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.|

## Columns

### Purchase_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

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
|Type|decimal(18, 3)|

### Confirmed_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Confirmed_Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Planned_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Purchase_Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Confirmed_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Confirmed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


