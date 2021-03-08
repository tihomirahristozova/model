# Table Prd_Workgroup_Shifts

Contains the working shifts of the wrokgroups. Entity: Prd_Workgroup_Shifts

# Aggregate Hierarchy

* [Prd_Workgroups](Prd_Workgroups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Efficiency_Factor_Percent|`Decimal`||Efficiency factor of the routing steps for this shift, expressed as percentage. `Required` `Default(1)` |
|Establishment_Date|`DateTime`||When the workgroup shift was established. Used as minimum date when generating calendar. `Required` `Default(Today)` `Filter(ge;le)` |
|Shift_Name|`String`||The name of the workgroup shift. `Required` `Filter(like)` |
