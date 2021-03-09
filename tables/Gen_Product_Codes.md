# Table Gen_Product_Codes

Additional product codes, categorized by coding systems. Entity: Gen_Product_Codes

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which the code is specified|
|[Coding_System_Id](#coding_system_id)|`uniqueidentifier` |The coding system in which the product code is specified|
|[Product_Code](#product_code)|`nvarchar(32)` |The code of the product in the specified coding system|
|[Active](#active)|`bit` |True when the code is active and can be selected in new documents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Coding_System_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


