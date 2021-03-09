# Table Prd_Workgroup_Shifts

Contains the working shifts of the wrokgroups. Entity: Prd_Workgroup_Shifts

## Owner Tables Hierarchy

* [Prd_Workgroups](Prd_Workgroups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique workgroup shift Id|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` ||
|[Shift_Name](#shift_name)|`nvarchar(254)` |The name of the workgroup shift.|
|[Establishment_Date](#establishment_date)|`datetime` |When the workgroup shift was established. Used as minimum date when generating calendar|
|[Work_Schedule_Id](#work_schedule_id)|`uniqueidentifier` |The work schedule used to calculate the working time for the shift.|
|[Efficiency_Factor_Percent](#efficiency_factor_percent)|`decimal(3, 2)` |Efficiency factor of the routing steps for this shift, expressed as percentage|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Shift_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Establishment_Date

| Property | Value |
| - | - |
|Type|datetime|

### Work_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Efficiency_Factor_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


