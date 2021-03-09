# Table Prd_Principal_Recipe_Operations

Contains the operations within a principal recipe. Entity: Prd_Principal_Recipe_Operations

## Owner Tables Hierarchy

* [Prd_Principal_Recipes](Prd_Principal_Recipes.md)
* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` |The generic operation definition. The data is copied locally and can be modified for this specific record.|
|[Operation_Description](#operation_description)|`nvarchar(2147483647)` |The description of the operation. Initially copied from the generic operation definition.|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |Required workgroup resource for the operation. NULL means that no resource is required or the resource will be specified later|
|[Use_Quantity](#use_quantity)|`decimal(9, 3)` |Quantity of the workgroup resource that should be allocated for the operation|
|[Use_Quantity_Unit_Id](#use_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Use_Quantity|
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of the previous operation can this operation start. NULL means that this operation should wait the previous operation to finish before starting|
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |Time needed to setup the equipment|
|[Run_Time_Minutes](#run_time_minutes)|`int` |Duration of the operation for one piece in the standard measurement unit of the product|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |Wait time (drying, cooling, etc.) after the operation in minutes|
|[Move_Time_Minutes](#move_time_minutes)|`int` |Time to move the lot to the next operation in minutes|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Standard rate of scrap during the operation|
|[Notes](#notes)|`nvarchar(254)` ||
|[Tooling](#tooling)|`nvarchar(254)` |The tools needed for the routing step|
|[Operation_Instruction_Id](#operation_instruction_id)|`uniqueidentifier` |Link to additional data, containing instructions in external format|
|[Line_Ord](#line_ord)|`int` |Consecutive line number within the principal recipe.|
|[Conditional_Property_Id](#conditional_property_id)|`uniqueidentifier` |When not NULL, specifies that, when creating recipe, the operation will be added only if this property is set for the main product|
|[Conditional_Property_Value](#conditional_property_value)|`nvarchar(254)` |The desired value of the Conditional Property. |
|[Conditional_Property_Description](#conditional_property_description)|`nvarchar(254)` `ML`|The desired description of the Conditional Property. |
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Use_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Minimum_Concurrent_Start_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Setup_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Run_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Wait_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Move_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Operation_Instruction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Conditional_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Conditional_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Conditional_Property_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


