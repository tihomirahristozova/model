# Procedure Prd_Work_Orders_Table_Load_Environment_Item_Operations


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item, containing the line.|
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Operation_Description](#operation_description)|`nvarchar` ||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` ||
|[Use_Quantity](#use_quantity)|`decimal(0, 0)` ||
|[Scheduled_Start_Date_Time](#scheduled_start_date_time)|`datetime` ||
|[Scheduled_End_Date_Time](#scheduled_end_date_time)|`datetime` ||
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` ||
|[Setup_Time_Minutes](#setup_time_minutes)|`int` ||
|[Run_Time_Minutes](#run_time_minutes)|`int` ||
|[Wait_Time_Minutes](#wait_time_minutes)|`int` ||
|[Move_Time_Minutes](#move_time_minutes)|`int` ||
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` ||
|[Actual_Start_Date_Time](#actual_start_date_time)|`datetime` ||
|[Actual_End_Date_Time](#actual_end_date_time)|`datetime` ||
|[Line_Ord](#line_ord)|`int` ||
|[Tooling](#tooling)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

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

### Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

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

### Actual_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Actual_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


