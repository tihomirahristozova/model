# Table Prd_Operation_Resources


## Owner Tables Hierarchy

* [Prd_Operations](Prd_Operations.md)
* [Prd_Operation_Groups](Prd_Operation_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Function_Id](#function_id)|`uniqueidentifier` |Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation.|
|[Lock_Quantity](#lock_quantity)|`decimal(18, 3)` |the quantity of the resource to be locked. The measurement unit is specified in the Prd_Functions table.Primary_Unit.|
|[Line_Ord](#line_ord)|`int` |The position of the line in the model|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Id

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


