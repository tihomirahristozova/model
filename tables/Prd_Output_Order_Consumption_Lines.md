# Table Prd_Output_Order_Consumption_Lines

The internal production consumption of materials. Used only for control purposes - for comparison with the active consumption orders. Warehouse and accounting are still updated only by Consumption Orders. Entity: Prd_Output_Order_Consumption_Lines

## Owner Tables Hierarchy

* [Prd_Output_Orders](Prd_Output_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Output_Order_Consumption_Line_Id](#output_order_consumption_line_id)|`uniqueidentifier` `PK`||
|[Output_Order_Id](#output_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Line_Work_Order_Id](#line_work_order_id)|`uniqueidentifier` |Work order for the line. Initially copied from the header (if there work order is not null)|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item, for which the consumption is recorded.|
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` |The operation in which the material was consumed. NULL = unknown|
|[Material_Id](#material_id)|`uniqueidentifier` |The consumed material|
|[Consumed_Quantity_For_Setup](#consumed_quantity_for_setup)|`decimal(18, 3)` |The consumed quantity of the material while setting up the operation.|
|[Consumed_Quantity_For_Run](#consumed_quantity_for_run)|`decimal(18, 3)` |The consumed quantity of the material for the operation.|
|[Consumed_Quantity_For_Scrap](#consumed_quantity_for_scrap)|`decimal(18, 3)` |The scrapped quantity of the material for this operation.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit for the consumed quantity for setup, run and scrap.|
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` |When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Output_Order_Consumption_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Output_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Line_Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumed_Quantity_For_Setup

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Consumed_Quantity_For_Run

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Consumed_Quantity_For_Scrap

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


