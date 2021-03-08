# Table Prd_Resources

Resource types available to production. Entity: Prd_Resources

# Aggregate Hierarchy

* [Prd_Resource_Groups](Prd_Resource_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Resource_Name|`String`||Name of the resource. `Required` `Filter(like)` |
|Notes|`String`||User notes for the resource. |
|Setup_Duration_Hours|`Decimal`||The usual duration of setup when changing production. `Required` `Default(0)` |
