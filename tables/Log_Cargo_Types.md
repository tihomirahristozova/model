# Table Log_Cargo_Types

Represents a cargo type. Different cargo types might require different types of vehicles or modes of transportartion. Entity: Log_Cargo_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cargo_Type_Id|`Guid`|`PK`, Readonly||
|Cargo_Type_Code|`String`||The unique code of the CargoType. `Required` `Filter(eq;like)` `ORD` |
|Cargo_Type_Name|`String`||The name of this CargoType. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this CargoType. |
