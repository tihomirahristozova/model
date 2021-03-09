# Table Scm_Receiving_Order_Lines

Contains detail records of Receiving Orders. Each line contains the receiving of a quantity of a product. Entity: Scm_Receiving_Order_Lines

## Owner Tables Hierarchy

* [Scm_Receiving_Orders](Scm_Receiving_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The received product.|
|[Quantity](#quantity)|`decimal(18, 3)` |The received quantity.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. Initially copied from the Default Measurement Unit of the Product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot of the received goods.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Notes](#notes)|`nvarchar(254)` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin in which to receive the goods.|
|[Confirmed_Quantity_Base](#confirmed_quantity_base)|`decimal(18, 3)` |The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product.|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |The equivalence of Quantity, in the base measurement category of the product.|
|[Confirmed_Quantity](#confirmed_quantity)|`decimal(18, 3)` |The final confirmed received quantity, after adjustments. It is used in all calculations for the order. Usually changed with adjustments to the receivemnt order, in regard to the warehouse receipt or the invoice. When null, its value is equal to Quantity.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` `PK`||
|[Finished](#finished)|`bit` |When true, denotes that this is the last receivement for this purchase order line and further receivements are not expected.|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |When not NULL, specifies that the product was selected using the specified product code record.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The name of the received product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` ||
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` |The purchase order line for which we are receiving quantity.|
|[Price_Per_Unit](#price_per_unit)|`decimal(14, 5)` |The unit price of the received products, in the documents currency.|
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` |When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.|
|[Line_Store_Id](#line_store_id)|`uniqueidentifier` |The store in which the goods are received.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total amount for the line. Equals to Quantity * Price_Per_Unit|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Row_Version](#row_version)|`timestamp` ||
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Confirmed_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Confirmed_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Receiving_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

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

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Confirmed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


