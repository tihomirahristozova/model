# Table Gen_Product_Variants

Contains definitions of different variants of a product. The variants are differentiated by color, size and style. Entity: Gen_Product_Variants

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Variant_Id|`Guid`|`PK`, Readonly||
|Bar_Code|`String`||When specified, it contains a bar code which uniquely identifies the product variant. `Filter(eq;like)` `ORD` |
|Product_Variant_Code|`String`|Readonly|The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style. `Required` `Filter(eq;like)` `ReadOnly` |
|Product_Variant_Name|`MultilanguageString`|Readonly|Product variant name. It is the concatenation of the names of the color, size and style. `ReadOnly` |
