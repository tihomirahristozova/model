# Table Wms_Warehouse_Locations

One physical location within a warehouse. Locations are the leaf elements of the rack structure of the warehouse. Entity: Wms_Warehouse_Locations (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Location_Id](#warehouse_location_id)|`uniqueidentifier` `PK`||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse containing the location.|
|[Warehouse_Zone_Id](#warehouse_zone_id)|`uniqueidentifier` |The zone, which contains the location.|
|[Location_Address](#location_address)|`nvarchar(32)` |The address of the location. Should be unique within the warehouse.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Zone_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Address

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


