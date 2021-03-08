# Table Gen_Variant_Colors

Contains the different colors, which can be assigned to product variants. Entity: Gen_Variant_Colors

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Variant_Color_Id|`Guid`|`PK`, Readonly||
|Variant_Color_Code|`String`||Unique code of the color. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD` |
|Variant_Color_Name|`MultilanguageString`||The name of this VariantColor. `Required` `Filter(eq;like)` `ORD` |
