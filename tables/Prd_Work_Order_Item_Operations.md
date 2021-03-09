# Table Prd_Work_Order_Item_Operations

The operations that are performed to produce the product. Entity: Prd_Work_Order_Item_Operations

## Owner Tables Hierarchy

* [Prd_Work_Order_Items](Prd_Work_Order_Items.md)
* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Order of the line within the work order routing|
|[Operation_Id](#operation_id)|`uniqueidentifier` |The performed operation.|
|[Operation_Description](#operation_description)|`nvarchar(2147483647)` |The short description of the operation.|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The resource that will be used for the operation. NULL means that no resource will be locked for the operation|
|[Use_Quantity](#use_quantity)|`decimal(9, 3)` |Quantity of the resource, that should be allocated for the operation|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Tooling](#tooling)|`nvarchar(2147483647)` |The tools needed for the routing step|
|[Actual_End_Date_Time](#actual_end_date_time)|`datetime` |The date/time when the operation has completed. NULL means that the operation is not completed.|
|[Actual_Start_Date_Time](#actual_start_date_time)|`datetime` |The date/time when the operation has started. NULL means that the has not started yet|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Projected scrap rate of the operation|
|[Move_Time_Minutes](#move_time_minutes)|`int` |Time to move the lot to the next operation in minutes|
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |Time needed to setup the equipment in minutes|
|[Run_Time_Minutes](#run_time_minutes)|`int` |Time for production of one lot of the produced item in minutes|
|[Notes](#notes)|`nvarchar(254)` ||
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting|
|[Scheduled_End_Date_Time](#scheduled_end_date_time)|`datetime` |The date/time when the operation is scheduled to complete. NULL means that there is still no plan when the operation will finish (for new orders only)|
|[Scheduled_Start_Date_Time](#scheduled_start_date_time)|`datetime` |The date/time when the operation is planned to start. NULL means that there is still no plan when to start the operaion (only for new work orders)|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item, containing the line.|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |Wait time (drying, cooling, etc.) after the operation in minutes|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

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

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Actual_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Actual_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Move_Time_Minutes

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Minimum_Concurrent_Start_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Wait_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


