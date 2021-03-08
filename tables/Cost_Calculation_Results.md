# Table Cost_Calculation_Results

Contains the results of cost calculations. Entity: Cost_Calculation_Results

# Aggregate Hierarchy

* [Cost_Calculations](Cost_Calculations.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Calculation_Result_Id|`Guid`|`PK`, Readonly||
|Full_Cost|`Decimal`||The full cost of the specified quantity. `Required` `Default(0)` |
|Line_No|`Int32`||Consecutive number of the line within the calculation. `Required` |
|Project_Id|`Guid?`||The Project to which the cost was allocated. When null, the cost was not allocated to any specific Project. `Filter(multi eq)` |
|Quantity|`Decimal`||The quantity of the product. `Required` `Default(0)` |
