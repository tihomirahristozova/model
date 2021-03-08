# Table Acc_Profit_Centers

Defines company profit centers and their relative weight for automatic balance transfers from cost centers. Entity: Acc_Profit_Centers

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Profit_Center_Id|`Guid`|`PK`, Readonly||
|Profit_Center_Name|`String`||The name of this ProfitCenter. `Required` `Filter(like)` |
|Notes|`String`||Notes for this ProfitCenter. |
|Relative_Weight|`Decimal`||The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)` |
