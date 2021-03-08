# Table Fleet_Vehicle_Set_Vehicles

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

# Aggregate Hierarchy

* [Fleet_Vehicle_Sets](Fleet_Vehicle_Sets.md)
* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Set_Vehicle_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this VehicleSetVehicle. `Filter(like)` |
|Ordinal_Pos|`Int32?`||Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. `Filter(ge;le)` |
