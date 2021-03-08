# Table Inv_Product_Valuation_Groups

Contains the available valuation groups for products. They are used in reconciliations, where all pluses and minuses within a valuation group are allowed to balance each other without fiscal effects. Without valuation groups, each product is balanced for itself and taxes are calculated for each surplus. Entity: Inv_Product_Valuation_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Valuation_Group_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this ProductValuationGroup. `Filter(like)` |
|Valuation_Group_Code|`String`||The unique code of the product valuation group. `Required` `Filter(eq;like)` `ORD` |
|Valuation_Group_Name|`MultilanguageString`||The name of the product valuation group. `Required` `Filter(eq;like)` |
