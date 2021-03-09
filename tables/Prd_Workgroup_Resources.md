# Table Prd_Workgroup_Resources

Describes the availability of resources in the active workgroups. Entity: Prd_Workgroup_Resources

## Owner Tables Hierarchy

* [Prd_Workgroups](Prd_Workgroups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |Id of the workgroup, containing the resource|
|[Resource_Id](#resource_id)|`uniqueidentifier` |The contained resource type|
|[Available_Quantity](#available_quantity)|`decimal(18, 3)` |Quantity available of the resource in this workgroup. The measurement unit is specified in Prd_Resources|
|[Notes](#notes)|`nvarchar(254)` |User notes for the workgroup resource|
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

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


