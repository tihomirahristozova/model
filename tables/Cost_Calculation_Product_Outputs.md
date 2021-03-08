# Table Cost_Calculation_Product_Outputs

Represents costs allocated to product outputs. Entity: Cost_Calculation_Product_Outputs

# Aggregate Hierarchy

* [Cost_Calculations](Cost_Calculations.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Calculation_Product_Output_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Consecutive number of the line within the calculation. `Required` |
|Project_Id|`Guid?`||The Project, which absorbed the cost. `Filter(multi eq)` |
|Quantity|`Decimal`||The quantity produced. `Required` `Default(0)` |
