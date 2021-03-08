# Table Prd_Capacity

Contains capacity of workgroup resources available for production. Entity: Prd_Capacity

# Aggregate Hierarchy

* [Prd_Workgroup_Resources](Prd_Workgroup_Resources.md)
* [Prd_Workgroups](Prd_Workgroups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Capacity_Id|`Guid`|`PK`, Readonly||
|Available_End_Time|`DateTime`||End of availability period during Calendar_Date. `Required` |
|Available_Start_Time|`DateTime`||Start of availability period during Calendar_Date. `Required` |
|Calendar_Date|`DateTime`||Date of the availability period. `Required` `Filter(ge;le)` |
