# Table Fleet_Maintenance_Plans

Defines the periodic maintenance plans and the conditions for performing the next maintenance. Entity: Fleet_Maintenance_Plans

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Plan_Id|`Guid`|`PK`, Readonly||
|Check_Days|`Int32?`||When not null, specifies the number of days between maintenances. |
|Check_Months|`Int32?`||When not null, specifies the number of months between maintenances. |
|Maintenance_Plan_Code|`String`||The unique code of the MaintenancePlan. `Required` |
|Is_Active|`Boolean`||True if the plan is active and can be selected from drop-downs. `Required` `Default(true)` `Introduced in version 18.2` |
|Mileage_Km|`Int32?`||When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur. |
|Maintenance_Plan_Name|`String`||Maintenance plan name (Multilanguage). `Required` |
|Notes|`String`||Notes for this MaintenancePlan. |
|Trip_Count|`Int32?`||When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur. |
