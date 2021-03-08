# Table Cost_Distribution_Results

Contains the results of a cost distribution calculation. Entity: Cost_Distribution_Results

# Aggregate Hierarchy

* [Cost_Distributions](Cost_Distributions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Distribution_Result_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Consecutive line number (within the cost distribution document) of the result. `Required` |
|Output_Line_No|`Int32`||The line number (within the document) of the output over which the cost is distributed. `Required` |
