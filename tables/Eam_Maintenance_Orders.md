# Table Eam_Maintenance_Orders

Orders for maintenance. It is performed by a single service center, but can contain many different types of maintenance for many assets. The document is Activity and as such is scheduled and visible in the main calendar. Entity: Eam_Maintenance_Orders (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Order_Id](#maintenance_order_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` ||
|[Service_Center_Id](#service_center_id)|`uniqueidentifier` |The service center, which will perform the maintenance.|
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, which will be maintained. NULL means that more than one asset will be maintained.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The type of maintenance, which will be performed. NULL means that will be more than one type of maintenance performed.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Maintenance_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


