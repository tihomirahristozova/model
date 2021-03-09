# Table Prd_Recipe_Operation_Resources


## Owner Tables Hierarchy

* [Prd_Recipe_Operations](Prd_Recipe_Operations.md)
* [Prd_Recipes](Prd_Recipes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Recipe_Operation_Id](#recipe_operation_id)|`uniqueidentifier` ||
|[Function_Id](#function_id)|`uniqueidentifier` |If specified, might be used as search criteria for setup of the resource usage of a workorder. Either this or Resource_Id must be specified|
|[Resource_Id](#resource_id)|`uniqueidentifier` |If specified, the routing step will always use the specified resource. Either this or Function_Id must be specified|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The exact workgroup resource that is engaged in the operation|
|[Lock_Quantity](#lock_quantity)|`decimal(18, 3)` |The quantity of the workgroup resource that should be locked|
|[Notes](#notes)|`nvarchar(254)` ||
|[Line_Ord](#line_ord)|`int` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Function_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lock_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


