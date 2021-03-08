# Table Acc_Cost_Centers

Defines cost centers and their relation to profit centers. Entity: Acc_Cost_Centers

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Center_Id|`Guid`|`PK`, Readonly||
|Cost_Center_Name|`String`||The name of this CostCenter. `Required` `Filter(like)` |
|Notes|`String`||Notes for this CostCenter. |
|Relative_Weight|`Decimal`||The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)` |
