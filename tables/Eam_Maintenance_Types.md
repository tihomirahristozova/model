# Table Eam_Maintenance_Types

Types of maintenances which can be scheduled and performed on the managed assets. Maintenances can be scheduled based on date and tracked parameter change. Entity: Eam_Maintenance_Types (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Type_Id|`Guid`|`PK`, Readonly||
|Maintenance_Type_Code|`String`||Unique code of the maintenance type. `Required` `Filter(eq;like)` `ORD` |
|Default_Parameter_Change|`Int32?`||Default positive change of the tracked parameter between two maintenances. null means, that maintenances are not scheduled based on parameter change. |
|Default_Schedule_Days|`Int32?`||Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). null means that there is no default schedule in days. |
|Default_Schedule_Months|`Int32?`||Specifies the maximum number of months between two maintenances. null means that there is no default schedule in months. |
|Description|`MultilanguageString`||Detailed description of the maintenance (multilanguage). |
|Maintenance_Type_Name|`MultilanguageString`||Multilanguage name of the maintenance type. `Required` `Filter(eq;like)` |
