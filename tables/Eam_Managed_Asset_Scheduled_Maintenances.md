# Table Eam_Managed_Asset_Scheduled_Maintenances

Contains the scheduled maintenances for the managed assets. Each maintenance can be planned based on date, parameter value or both. Past maintenance plans are kept only for reference and can be deleted at any time. Entity: Eam_Managed_Asset_Scheduled_Maintenances (Introduced in version 19.1)

# Aggregate Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Scheduled_Maintenance_Id|`Guid`|`PK`, Readonly||
|Date|`DateTime?`||The date, when the maintenance is planned. null means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)` |
|Is_Dismissed|`Boolean`||Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action. `Required` `Default(false)` `Filter(multi eq)` |
|Notes|`String`||Notes for this ManagedAssetScheduledMaintenance. |
|Tracked_Parameter_Value|`Int32?`||The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. null means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)` |
