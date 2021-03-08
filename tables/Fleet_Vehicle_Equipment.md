# Table Fleet_Vehicle_Equipment

Contains the actual and history of equipment, installed on the vehicles. Entity: Fleet_Vehicle_Equipment

# Aggregate Hierarchy

* [Fleet_Vehicles](Fleet_Vehicles.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Equipment_Id|`Guid`|`PK`, Readonly||
|End_Date|`DateTime?`||The date when the equipment was removed. null when the equipment is still installed on the vehicle. `Filter(ge;le)` |
|Notes|`String`||Notes for the installed equipment. |
|Quantity|`Int32`||Quantity of the equipment. `Required` `Default(1)` `Filter(ge;le)` |
|Start_Date|`DateTime`||The installation date of the equipment. `Required` `Filter(ge;le)` |
