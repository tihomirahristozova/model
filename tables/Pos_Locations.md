# Table Pos_Locations

Defines a company location as POS enabled location. Entity: Pos_Locations (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Location_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Indicates whether the POS location is currently active and can be chosen in drop-downs, etc. `Default(true)` `Filter(eq)` |
|Pos_Location_Code|`String`||Unique (with the enterprise company) code of this POS location. `Required` `Filter(multi eq;like)` |
