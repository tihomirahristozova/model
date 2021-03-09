# Table Log_Shipment_Order_Lines

Represents detail lines of orders for shipment of sales orders to customers. Each line orders the shipment of one product. Entity: Log_Shipment_Order_Lines

## Owner Tables Hierarchy

* [Log_Shipment_Orders](Log_Shipment_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Shipment_Order_Line_Id](#shipment_order_line_id)|`uniqueidentifier` `PK`||
|[Shipment_Order_Id](#shipment_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Line number, unique for the shipment|
|[Parent_Sales_Order_Line_Id](#parent_sales_order_line_id)|`uniqueidentifier` |Sales order line which is shipped|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity to be shipped|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Finished](#finished)|`bit` |1 if this shipment should prohibit further shipments for the sales order line|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin from which to take the goods|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The store lot from which to take the goods|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number of the shipped product. NULL means that serial number is unknown or not applicable.|
|[Net_Weight_kg](#net_weight_kg)|`decimal(12, 3)` |The net weight of the entire batch of goods in kilograms. NULL means unknown|
|[Gross_Weight_kg](#gross_weight_kg)|`decimal(12, 3)` |The gross weight of the whole line in kilogramms. NULL means unknown|
|[Volume_l](#volume_l)|`decimal(12, 3)` |The volume in litres of the whole batch. NULL means unknown|
|[Height_m](#height_m)|`decimal(12, 3)` |The height of the package in meters. NULL means unknown|
|[Length_m](#length_m)|`decimal(12, 3)` |The length of the package in meters. NULL means unknown|
|[Width_m](#width_m)|`decimal(12, 3)` |The width of the package in meters. NULL means unknown|
|[Pallet_No](#pallet_no)|`int` |The number of the pallet in which the goods are packaged. NULL means unknown|
|[Box_Count](#box_count)|`int` |The count of boxes in which the goods are packaged. NULL means unknown|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalence of Quantity in the base measurement category of the product.|
|[Persist_Lot](#persist_lot)|`bit` |If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document.|
|[Row_Version](#row_version)|`timestamp` ||
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Shipment_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Shipment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Store_Bin_Id

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

### Net_Weight_kg

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Gross_Weight_kg

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Volume_l

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Height_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Length_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Width_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Pallet_No

| Property | Value |
| - | - |
|Type|int|

### Box_Count

| Property | Value |
| - | - |
|Type|int|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Persist_Lot

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


