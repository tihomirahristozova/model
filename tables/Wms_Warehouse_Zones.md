# Table Wms_Warehouse_Zones

One zone within a warehouse. Each zone can have different rack structure and different temperature and other properties. Entity: Wms_Warehouse_Zones (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Zone_Id](#warehouse_zone_id)|`uniqueidentifier` `PK`||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse in which the zone is located.|
|[Warehouse_Zone_Name](#warehouse_zone_name)|`nvarchar(254)` `ML`|Multi-language name of the zone.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Warehouse_Zone_Id](#parent_warehouse_zone_id)|`uniqueidentifier` |The parent Warehouse Zone of the current Warehouse Zone.|
|[Warehouse_Zone_Code](#warehouse_zone_code)|`nvarchar(32)` |Zone code, unique within the warehouse.|

## Columns

### Warehouse_Zone_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Zone_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Parent_Warehouse_Zone_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Zone_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|


