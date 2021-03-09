# Table Prd_Operations

The different steps performed to create products. Entity: Prd_Operations

## Owner Tables Hierarchy

* [Prd_Operation_Groups](Prd_Operation_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Operation_Group_Id](#operation_group_id)|`uniqueidentifier` ||
|[Operation_Name](#operation_name)|`nvarchar(50)` ||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |When not NULL, specifies the Workgroup Resource, which is required by the operation.|
|[Use_Quantity_Base](#use_quantity_base)|`decimal(9, 3)` |Quantity of the resource that need to be allocated for the operation, in base measurement units for the resource|
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting|
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |The time required to setup the operation. The setup is incurred only once, regardless of the produced quntity.|
|[Run_Time_Minutes](#run_time_minutes)|`int` |The time required to process one product lot. The run time is calculated for each produced lot.|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |The time required to wait after completing the operation. During this time, the resource is still allocated to the operation.|
|[Move_Time_Minutes](#move_time_minutes)|`int` |The time required for the product to move to the next operation. During this time no resource is allocated.|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |The percentage (0..1) of scrap usually occurring during the production operation. NULL means that the scrap rate cannot be generally calculated.|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Tooling](#tooling)|`nvarchar(254)` |Short description of the needed instruments for the operation.|
|[Operation_Instructions_Id](#operation_instructions_id)|`uniqueidentifier` |Full instructions for the operation.|
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(18, 6)` |Standard price for 1 hour work for this operation.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

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

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Operation_Instructions_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


