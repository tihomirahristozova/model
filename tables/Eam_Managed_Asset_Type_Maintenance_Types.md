# Table Eam_Managed_Asset_Type_Maintenance_Types

Defines the types of maintenances, which are allowed for assets of the different types. Entity: Eam_Managed_Asset_Type_Maintenance_Types (Introduced in version 19.1)

# Aggregate Hierarchy

* [Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Type_Maintenance_Type_Id|`Guid`|`PK`, Readonly||
|Default_Parameter_Change|`Int32?`||Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means, that maintenances are not scheduled based on parameter change. |
|Default_Schedule_Days|`Int32?`||Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in days. |
|Default_Schedule_Months|`Int32?`||Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in months. |
|Notes|`String`||Notes for this ManagedAssetTypeMaintenanceType. |
