# Table Log_Transportation_Vehicles

A vehicle, which is used for transportation. One actual vehicle might be defined multiple times as transportation vehicle - for different modes of transportation or cargo types. Entity: Log_Transportation_Vehicles

# Aggregate Hierarchy

* [Fleet_Vehicles](Fleet_Vehicles.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Vehicle_Id|`Guid`|`PK`, Readonly||
|Code|`String`||The unique code (or call sign) of this transportation vehicle. `Required` `Filter(eq;like)` `ORD` |
|Max_Cargo_Weight_Kg|`Int32?`||The maximum weight of the cargo (in kg), which can be transported. null when this is unknown and no limit should be enforced. |
|Max_Pallets_Count|`Int32?`||The maximum number of pallets, which can be transported by the vehicle. null when this is unknown and no limit should be enforced. |
|Notes|`String`||Notes for this TransportationVehicle. |
