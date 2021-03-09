# Table Prd_Functions

Definition of the functions that the resources can perform. Entity: Prd_Functions

## Owner Tables Hierarchy

* [Prd_Function_Groups](Prd_Function_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Function_Group_Id](#function_group_id)|`uniqueidentifier` ||
|[Function_Name](#function_name)|`nvarchar(64)` ||
|[Primary_Unit](#primary_unit)|`uniqueidentifier` |Primary measurement unit for measuring workload of the function. Resources that can perform the function should be measureable in this unit|
|[Notes](#notes)|`nvarchar(254)` |User comments on the function|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Function_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Function_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Primary_Unit

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


