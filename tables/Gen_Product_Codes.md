# Table Gen_Product_Codes

Additional product codes, categorized by coding systems. Entity: Gen_Product_Codes

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Code_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True when the code is active and can be selected in new documents. `Required` `Default(true)` `Filter(eq)` |
|Product_Code|`String`||The code of the product in the specified coding system. `Required` `Filter(eq;like)` |
