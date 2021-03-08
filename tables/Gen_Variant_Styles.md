# Table Gen_Variant_Styles

Contains the different styles, which can be assigned to product variants. Entity: Gen_Variant_Styles

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Variant_Style_Id|`Guid`|`PK`, Readonly||
|Variant_Style_Code|`String`||Unique code of the style. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD` |
|Variant_Style_Name|`MultilanguageString`||The name of this VariantStyle. `Required` `Filter(eq;like)` `ORD` |
