# Table Cost_Calculation_Results

Contains the results of cost calculations. Entity: Cost_Calculation_Results

## Owner Tables Hierarchy

* [Cost_Calculations](Cost_Calculations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the calculation|
|[Calculation_Result_Id](#calculation_result_id)|`uniqueidentifier` `PK`||
|[Calculation_Id](#calculation_id)|`uniqueidentifier` ||
|[Project_Id](#project_id)|`uniqueidentifier` |The Project to which the cost was allocated. When NULL, the cost was not allocated to any specific Project.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |The Sales Order to which the cost was allocated. When NULL, the cost was not allocated to any specific Sales Order.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product to which the cost was allocated. When NULL, the cost was not allocated to any specific Product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Lot to which the cost was allocated. When NULL, the cost was not allocated to any specific Lot.|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The Profit Center to which the cost was allocated. When NULL, the cost was not allocated to any specific Profit Center.|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The Workgroup to which the cost was allocated. When NULL, the cost was not allocated to any specific Workgroup.|
|[Quantity](#quantity)|`decimal(14, 3)` |The quantity of the product|
|[Full_Cost](#full_cost)|`decimal(14, 2)` |The full cost of the specified quantity|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Calculation_Result_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calculation_Id

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

### Quantity

| Property | Value |
| - | - |
|Type|decimal(14, 3)|

### Full_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


