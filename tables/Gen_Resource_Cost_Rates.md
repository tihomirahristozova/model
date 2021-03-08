# Table Gen_Resource_Cost_Rates

Contains cost rates for different periods for resources. Each record is valid until the next From Date. Entity: Gen_Resource_Cost_Rates

# Aggregate Hierarchy

* [Gen_Resources](Gen_Resources.md)
* [Gen_Resource_Groups](Gen_Resource_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Resource_Cost_Rate_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime`||Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined. `Required` `Filter(eq;ge;le)` |
|Notes|`String`||Notes for this ResourceCostRate. |
