# Table Ast_Asset_Categories

Categorization of the assets, which specifies their depreciation plans. Entity: Ast_Asset_Categories

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Category_Id](#asset_category_id)|`uniqueidentifier` `PK`||
|[Asset_Category_Code](#asset_category_code)|`nvarchar(20)` ||
|[Asset_Category_Name](#asset_category_name)|`nvarchar(254)` ||
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` |Product type that correspondes to this category. Depreciation plan templates specified for this category will be used for the products of this type.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Category_Code

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Asset_Category_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


