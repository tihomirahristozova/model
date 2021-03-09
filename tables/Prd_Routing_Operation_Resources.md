# Table Prd_Routing_Operation_Resources


## Owner Tables Hierarchy

* [Prd_Routing_Operations](Prd_Routing_Operations.md)
* [Prd_Routings](Prd_Routings.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Routing_Operation_Id](#routing_operation_id)|`uniqueidentifier` |The routing operation, containing the line|
|[Function_Id](#function_id)|`uniqueidentifier` |Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation.|
|[Lock_Quantity](#lock_quantity)|`decimal(18, 3)` |the quantity of the resource to be locked. The measurement unit is specified in the Prd_Functions table.Primary_Unit.|
|[Line_Ord](#line_ord)|`int` |The position of the line in the recipe model|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Function_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lock_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


