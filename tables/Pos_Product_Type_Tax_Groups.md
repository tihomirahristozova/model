# Table Pos_Product_Type_Tax_Groups

Contains the tax group codes for the product types. The tax group codes are used when sales documents are printed to fiscal printers or exported to fiscal authorities. Entity: Pos_Product_Type_Tax_Groups (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Gen_Product_Types](Gen_Product_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Type_Tax_Group_Id](#product_type_tax_group_id)|`uniqueidentifier` `PK`||
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` |The product type for which the tax group is specified.|
|[Applicable_Legislation](#applicable_legislation)|`nvarchar(8)` Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|The legislation, for which the tax group is applicable.|
|[Tax_Group](#tax_group)|`int` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|The tax group of the product type within the specified applicable legislation.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Type_Tax_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Applicable_Legislation

| Property | Value |
| - | - |
|Type|nvarchar(8)|

### Tax_Group

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


