# Table Fleet_Maintenance_Profiles

Profiles contain multiple maintenance plans and can be assigned directly to a vehicle. Entity: Fleet_Maintenance_Profiles

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Profile_Id|`Guid`|`PK`, Readonly||
|Maintenance_Profile_Code|`String`||The unique code of the MaintenanceProfile. `Required` |
|Is_Active|`Boolean`||True if the profile is active and can be assigned to vehicles. However, if a profile is already assigned to a vehicle, it will still work even if it is de-activated. `Required` `Default(true)` `Introduced in version 18.2` |
|Maintenance_Profile_Name|`String`||Name of the maintenance profile (Multilanguage). `Required` |
|Notes|`String`||Notes for this MaintenanceProfile. |
