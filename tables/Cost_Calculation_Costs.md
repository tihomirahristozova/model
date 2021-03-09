# Table Cost_Calculation_Costs

Contains the calculated costs allocated to the different Cost Types. Entity: Cost_Calculation_Costs

## Owner Tables Hierarchy

* [Cost_Calculations](Cost_Calculations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the calculation|
|[Calculation_Cost_Id](#calculation_cost_id)|`uniqueidentifier` `PK`||
|[Calculation_Id](#calculation_id)|`uniqueidentifier` ||
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The Cost Type, which absorbed the cost.|
|[Amount](#amount)|`decimal(14, 2)` |The allocated amount of costs in the currency of the calculation.|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |The Cost Center, which absorbed the cost.|
|[Project_Id](#project_id)|`uniqueidentifier` |The Project, which absorbed the cost.|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The Workgroup, which absorbed the cost.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |The Sales Order, which absorbed the cost.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product, which absorbed the cost.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Lot, which absorbed the cost.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Calculation_Cost_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calculation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


