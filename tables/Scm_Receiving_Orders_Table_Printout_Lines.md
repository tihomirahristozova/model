# Procedure Scm_Receiving_Orders_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` ||
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` `PK`||
|[POL_Product_Name](#pol_product_name)|`nvarchar` `ML`|Name of the item|
|[Purchase_Order_Line_Id_Text](#purchase_order_line_id_text)|`nvarchar` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot of the received goods.|
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` |When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.|
|[Line_Store_Id](#line_store_id)|`uniqueidentifier` |The store in which the goods are received.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total amount for the line. Equals to Quantity * Price_Per_Unit|
|[Price_Per_Unit](#price_per_unit)|`decimal(14, 5)` |The unit price of the received products, in the documents currency.|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` `ML`|Name of the measurement unit|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. Initially copied from the Default Measurement Unit of the Product.|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Quantity](#quantity)|`decimal(18, 3)` |The received quantity.|
|[Product_Description](#product_description)|`nvarchar` `ML`|The name of the received product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Product_Id_Text](#product_id_text)|`nvarchar` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The received product.|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` ||
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` |The purchase order line for which we are receiving quantity.|
|[POL_Quantity](#pol_quantity)|`decimal(0, 0)` ||
|[POL_Price_Per_Unit](#pol_price_per_unit)|`decimal(0, 0)` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Receiving_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### POL_Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Order_Line_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### POL_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### POL_Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


