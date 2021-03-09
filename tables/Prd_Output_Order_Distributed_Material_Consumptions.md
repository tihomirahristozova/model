# Table Prd_Output_Order_Distributed_Material_Consumptions

Contains the quantity of materials distributed over the output order lines. Entity: Prd_Output_Order_Distributed_Material_Consumptions

## Owner Tables Hierarchy

* [Prd_Output_Order_Lines](Prd_Output_Order_Lines.md)
* [Prd_Output_Orders](Prd_Output_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Output_Order_Line_Id](#output_order_line_id)|`uniqueidentifier` Readonly|The output order line for which the distribution is recorded.|
|[Consumption_Order_Line_Id](#consumption_order_line_id)|`uniqueidentifier` Readonly|Consumption order line which requested the Consumed_Quantity|
|[Consumed_Quantity](#consumed_quantity)|`decimal(18, 3)` Readonly|Part of the quantity in the consumption order line which was used for the product in the output order line|
|[Consumed_Cost](#consumed_cost)|`decimal(14, 2)` Readonly|Cost of the actually issued Consumed_Quantity|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Output_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumption_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumed_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Consumed_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


