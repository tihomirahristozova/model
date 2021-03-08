# Table Gen_Product_Dimensions

Contains convertion ratios between the supported measument categories for each product. Does not contain a record for the default category of the products, for which the convertion ratio is defined as equal to 1. Entity: Gen_Product_Dimensions

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Dimension_Id|`Guid`|`PK`, Readonly||
|Convert_To_Base_Divisor|`Decimal`||This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required` |
|Convert_To_Base_Multiplier|`Decimal`||This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required` |
