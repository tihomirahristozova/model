# Table Prj_Type_Work_Types

Contains the work types, that can be performed in projects of this project type. Entity: Prj_Type_Work_Types

# Aggregate Hierarchy

* [Prj_Types](Prj_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Work_Type_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||True when the work type is currently active and selectable in new documents. `Required` `Default(true)` `Filter(eq)` |
|Work_Type_Name|`String`||The name of the work type. `Required` `Filter(eq;like)` |
