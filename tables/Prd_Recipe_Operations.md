# Table Prd_Recipe_Operations

Contains the routing (operation list) of the recipes. Entity: Prd_Recipe_Operations

## Owner Tables Hierarchy

* [Prd_Recipes](Prd_Recipes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Order of the operation within the recipe|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(18, 6)` |Standard price for 1 hour work|
|[Operation_Instruction_Id](#operation_instruction_id)|`uniqueidentifier` |Link to additional data, containing instructions in external format|
|[Tooling](#tooling)|`nvarchar(2147483647)` |The tools needed for the routing step|
|[Notes](#notes)|`nvarchar(254)` ||
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Standard rate of scrap during the operation|
|[Move_Time_Minutes](#move_time_minutes)|`int` |Time to move the lot to the next operation in minutes|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |Wait time (drying, cooling, etc.) after the operation in minutes|
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(18, 6)` |Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe.|
|[Run_Time_Minutes](#run_time_minutes)|`int` |Duration of the operation for standard lot of the product|
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting|
|[Use_Quantity_Unit_Id](#use_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Use_Quantity|
|[Use_Quantity](#use_quantity)|`decimal(9, 3)` |Quantity of the workgroup resource that should be allocated for the operation|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The exact workgroup resource that is engaged in the operation. NULL means that no resource is needed or it will be specfied at a later stage|
|[Operation_Description](#operation_description)|`nvarchar(2147483647)` |The description of the operation.|
|[Operation_Id](#operation_id)|`uniqueidentifier` |Standard operation Id. If not NULL used to load the details. If NULL the details (times, scrap rates, etc.) must be entered manually|
|[Routing_Operation_Id](#routing_operation_id)|`uniqueidentifier` ||
|[Recipe_Id](#recipe_id)|`uniqueidentifier` ||
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |Time needed to setup the equipment|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Operation_Instruction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Move_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Wait_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Standard_Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Run_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Minimum_Concurrent_Start_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Use_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Setup_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


