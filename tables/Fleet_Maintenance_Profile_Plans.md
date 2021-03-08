# Table Fleet_Maintenance_Profile_Plans

Contains the plans, included in the maintenance profile. Entity: Fleet_Maintenance_Profile_Plans

# Aggregate Hierarchy

* [Fleet_Maintenance_Profiles](Fleet_Maintenance_Profiles.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Profile_Plan_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. `Required` `Default(true)` `Introduced in version 18.2` |
|Notes|`String`||Notes for this MaintenanceProfilePlan. |
