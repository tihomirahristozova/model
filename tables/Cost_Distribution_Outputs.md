# Table Cost_Distribution_Outputs

Contains the output data for the specified period. This is the output on which cost is distributed. Entity: Cost_Distribution_Outputs

# Aggregate Hierarchy

* [Cost_Distributions](Cost_Distributions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Distribution_Output_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Unique (within the document), consecutive line number of the output. `Required` |
|Weight_Coefficient|`Decimal`||The weight coefficient for prorate distribution of cost over the current line. `Required` `Default(1)` |
