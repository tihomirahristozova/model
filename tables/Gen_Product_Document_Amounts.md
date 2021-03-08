# Table Gen_Product_Document_Amounts

Contains custom percent ratios for additional amount distribution over products. Entity: Gen_Product_Document_Amounts

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Document_Amount_Id|`Guid`|`PK`, Readonly||
|Line_Percent|`Decimal`||The custom percent for the current product and amount type. `Required` `Default(0)` |
