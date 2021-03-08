# Table Fleet_Crews

Represents the crews, which can operate vehicles. Entity: Fleet_Crews

# Aggregate Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Crew_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||Is the crew active? true-active for choosing; false-otherwise. `Required` `Default(true)` `Filter(eq)` |
|Crew_Name|`MultilanguageString`||The name of the crew (multilanguage). `Required` `Filter(eq;like)` |
