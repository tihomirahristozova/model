# Table Eam_Maintenance_Type_Groups

Represents the hierarchy of the groups of maintenance types. Entity: Eam_Maintenance_Type_Groups (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Type_Group_Id|`Guid`|`PK`, Readonly||
|Maintenance_Type_Group_Code|`String`||Unique code of the group. `Required` `Filter(eq;like)` `ORD` |
|Maintenance_Type_Group_Name|`MultilanguageString`||Multilanguage name of the group. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this MaintenanceTypeGroup. |
