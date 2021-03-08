# Table Eam_Managed_Asset_Maintenance_Schedules

Contains the maintenance schedules for the managed assets. Entity: Eam_Managed_Asset_Maintenance_Schedules (Introduced in version 19.1)

# Aggregate Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Maintenance_Schedule_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this ManagedAssetMaintenanceSchedule. |
|Parameter_Change_Delta|`Int32?`||The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. null means, that the maintenances are not planned, based on parameter change. `Filter(multi eq;ge;le)` |
|Schedule_Days|`Int32?`||Number of days between planned maintenances. null means that the schedule is not planned based on days. |
|Schedule_Months|`Int32?`||Number of months between planned maintenances. null means that the schedule is not planned based on months. |
