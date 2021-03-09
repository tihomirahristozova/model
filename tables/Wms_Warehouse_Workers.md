# Table Wms_Warehouse_Workers

Human or robot worker, which can execute warehouse tasks. Entity: Wms_Warehouse_Workers (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Worker_Id](#warehouse_worker_id)|`uniqueidentifier` `PK`||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse, where the worker works.|
|[Warehouse_Worker_Name](#warehouse_worker_name)|`nvarchar(254)` `ML`|Name of the worker (multi-language).|
|[Person_Id](#person_id)|`uniqueidentifier` |The definition of the person, when the worker is human worker. NULL means that the person is unknown or the worker is non-person.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the worker is active and can execute new warehouse tasks.|
|[Active_From](#active_from)|`date` |The date, from which the worker record has become active in the warehouse.|
|[Active_To](#active_to)|`date` |The date of termination of the activity of the worker in the warehouse. Can be NULL for workers, which are still active and do not have previous terminations.|

## Columns

### Warehouse_Worker_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Worker_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Active_From

| Property | Value |
| - | - |
|Type|date|

### Active_To

| Property | Value |
| - | - |
|Type|date|


