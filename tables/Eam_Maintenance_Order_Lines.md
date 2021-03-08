# Table Eam_Maintenance_Order_Lines

Contains the types of maintenance and maintained assets in the maintenance orders. Entity: Eam_Maintenance_Order_Lines (Introduced in version 19.1)

# Aggregate Hierarchy

* [Eam_Maintenance_Orders](Eam_Maintenance_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Order_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Consecutive line number, unique within the maintenance order. `Required` |
|Next_Service_Date|`DateTime?`||Specifies, that the maintenance required a specific date for the next maintenance. null means that default scheduling should be used. |
|Next_Service_Tracked_Parameter_Value|`Int32?`||Specifies, that the maintenance required the next maintenance to be performed on a specific value of the tracked parameter. null means that default scheduling should be used. |
|Notes|`String`||Notes for this MaintenanceOrderLine. |
