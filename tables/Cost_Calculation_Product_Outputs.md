# Table Cost_Calculation_Product_Outputs

Represents costs allocated to product outputs. Entity: Cost_Calculation_Product_Outputs

## Owner Tables Hierarchy

* [Cost_Calculations](Cost_Calculations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the calculation|
|[Calculation_Product_Output_Id](#calculation_product_output_id)|`uniqueidentifier` `PK`||
|[Calculation_Id](#calculation_id)|`uniqueidentifier` ||
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity produced|
|[Parent_Calculation_Product_Output_Id](#parent_calculation_product_output_id)|`uniqueidentifier` |When not NULL specifies the parent output, whose cost is "absorbed" within the current output.|
|[Project_Id](#project_id)|`uniqueidentifier` |The Project, which absorbed the cost.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |The Sales Order, which absorbed the cost.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product, which absorbed the cost.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Lot, which absorbed the cost.|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The Profit Center, which absorbed the cost.|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The Workgroup, which absorbed the cost.|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The Work Order, which absorbed the cost.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Calculation_Product_Output_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calculation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Parent_Calculation_Product_Output_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


