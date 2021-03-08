# Table Cost_Calculation_Costs

Contains the calculated costs allocated to the different Cost Types. Entity: Cost_Calculation_Costs

# Aggregate Hierarchy

* [Cost_Calculations](Cost_Calculations.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Calculation_Cost_Id|`Guid`|`PK`, Readonly||
|Amount|`Decimal`||The allocated amount of costs in the currency of the calculation. `Required` `Default(0)` |
|Line_No|`Int32`||Consecutive number of the line within the calculation. `Required` |
|Project_Id|`Guid?`||The Project, which absorbed the cost. `Filter(multi eq)` |
