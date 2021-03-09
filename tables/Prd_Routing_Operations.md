# Table Prd_Routing_Operations


## Owner Tables Hierarchy

* [Prd_Routings](Prd_Routings.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Routing_Id](#routing_id)|`uniqueidentifier` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` |The oepration that should be performed|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Scrap rate of the routing operation. Initially it is copied from the operation definition|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The allocated resource for the operation. If NULL - no resource is needed|
|[Duration_Hour](#duration_hour)|`decimal(10, 0)` |The approximate duration of the operation (for quantity of 1) in seconds. This is pure operation time and excludes setup time.|
|[Line_Ord](#line_ord)|`int` |Order of the line within the routing|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Duration_Hour

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


