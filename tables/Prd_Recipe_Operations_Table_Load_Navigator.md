# Query Prd_Recipe_Operations_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Recipe_Name](#recipe_name)|`nvarchar` ||
|[Release_Date](#release_date)|`datetime` ||
|[Expiry_Date](#expiry_date)|`datetime` ||
|[Produce_Quantity](#produce_quantity)|`decimal(0, 0)` ||
|[Routing_Id](#routing_id)|`uniqueidentifier` ||
|[Price_Per_Lot](#price_per_lot)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` ||
|[Store_Id](#store_id)|`uniqueidentifier` |The store for which this technology is valid. The store is matched with the output store specified in the production order. When NULL, the technology is valid for all stores.|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Recipe_Id](#recipe_id)|`uniqueidentifier` ||
|[Routing_Operation_Id](#routing_operation_id)|`uniqueidentifier` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Operation_Description](#operation_description)|`nvarchar` ||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` ||
|[Use_Quantity](#use_quantity)|`decimal(0, 0)` ||
|[Use_Quantity_Unit_Id](#use_quantity_unit_id)|`uniqueidentifier` ||
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` ||
|[Setup_Time_Minutes](#setup_time_minutes)|`int` ||
|[Run_Time_Minutes](#run_time_minutes)|`int` ||
|[Wait_Time_Minutes](#wait_time_minutes)|`int` ||
|[Move_Time_Minutes](#move_time_minutes)|`int` ||
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` ||
|[Recipe_Operations_Notes](#recipe_operations_notes)|`nvarchar` ||
|[Tooling](#tooling)|`nvarchar` ||
|[Operation_Instruction_Id](#operation_instruction_id)|`uniqueidentifier` ||
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(0, 0)` ||
|[Line_Ord](#line_ord)|`int` ||
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(0, 0)` |Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe.|
|[Row_Version](#row_version)|`timestamp` ||
|[Produce_Quantity_AMU](#produce_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||

## Columns

### Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Produce_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Routing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Operation_Id

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
|Type|nvarchar|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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
|Type|decimal(0, 0)|

### Recipe_Operations_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar|

### Operation_Instruction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Standard_Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Produce_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


