# Table Fleet_Vehicle_Sets

Represents sets of vehicles, which can travel together. Entity: Fleet_Vehicle_Sets

# Aggregate Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Set_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True if the vehicle set is active for choosing; false - otherwise. `Required` `Default(true)` `Filter(eq)` |
|Vehicle_Set_Name|`MultilanguageString`||Name of the vehicle set (Multilanguage). `Required` `Filter(eq;like)` |
