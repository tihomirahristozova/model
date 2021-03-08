# Table Gen_Variant_Sizes

Contains the different sizes, which can be assigned to product variants. Entity: Gen_Variant_Sizes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Variant_Size_Id|`Guid`|`PK`, Readonly||
|Variant_Size_Code|`String`||Unique code of the size. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD` |
|Variant_Size_Name|`MultilanguageString`||The name of the variant size. `Required` `Filter(eq;like)` `ORD` |
