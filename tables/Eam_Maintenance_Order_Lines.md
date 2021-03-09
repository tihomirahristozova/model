# Table Eam_Maintenance_Order_Lines

Contains the types of maintenance and maintained assets in the maintenance orders. Entity: Eam_Maintenance_Order_Lines (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Maintenance_Orders](Eam_Maintenance_Orders.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the maintenance order.|
|[Maintenance_Order_Line_Id](#maintenance_order_line_id)|`uniqueidentifier` `PK`||
|[Maintenance_Order_Id](#maintenance_order_id)|`uniqueidentifier` ||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The maintained asset.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The type of maintenance performed.|
|[Next_Service_Date](#next_service_date)|`date` |Specifies, that the maintenance required a specific date for the next maintenance. NULL means that default scheduling should be used.|
|[Next_Service_Tracked_Parameter_Value](#next_service_tracked_parameter_value)|`int` |Specifies, that the maintenance required the next maintenance to be performed on a specific value of the tracked parameter. NULL means that default scheduling should be used.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Maintenance_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Order_Id

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

### Next_Service_Date

| Property | Value |
| - | - |
|Type|date|

### Next_Service_Tracked_Parameter_Value

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


