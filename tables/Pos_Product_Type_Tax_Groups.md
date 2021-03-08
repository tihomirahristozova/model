# Table Pos_Product_Type_Tax_Groups

Contains the tax group codes for the product types. The tax group codes are used when sales documents are printed to fiscal printers or exported to fiscal authorities. Entity: Pos_Product_Type_Tax_Groups (Introduced in version 19.1)

# Aggregate Hierarchy

* [Gen_Product_Types](Gen_Product_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Type_Tax_Group_Id|`Guid`|`PK`, Readonly||
|Applicable_Legislation|`ApplicableLegislation`|Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|The legislation, for which the tax group is applicable. `Required` `Filter(multi eq)` |
|Notes|`String`||Notes for this ProductTypeTaxGroup. `Filter(eq;like)` |
|Tax_Group|`TaxGroup`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|The tax group of the product type within the specified applicable legislation. `Required` `Filter(multi eq)` |
