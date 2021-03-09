# Table Prd_Capacity

Contains capacity of workgroup resources available for production. Entity: Prd_Capacity

## Owner Tables Hierarchy

* [Prd_Workgroup_Resources](Prd_Workgroup_Resources.md)
* [Prd_Workgroups](Prd_Workgroups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Capacity_Id](#capacity_id)|`uniqueidentifier` `PK`||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The capacity-constrained resource|
|[Calendar_Date](#calendar_date)|`datetime` |Date of the availability period|
|[Available_Start_Time](#available_start_time)|`datetime` |Start of availability period during Calendar_Date|
|[Available_End_Time](#available_end_time)|`datetime` |End of availability period during Calendar_Date|
|[Available_Quantity](#available_quantity)|`decimal(9, 0)` |Quantity of the resource, available to production|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Capacity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calendar_Date

| Property | Value |
| - | - |
|Type|datetime|

### Available_Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Available_End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Available_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


