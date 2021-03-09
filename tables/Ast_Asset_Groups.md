# Table Ast_Asset_Groups

User-defined grouping of the assets. Entity: Ast_Asset_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Group_Id](#asset_group_id)|`uniqueidentifier` `PK`||
|[Parent_Asset_Group_Id](#parent_asset_group_id)|`uniqueidentifier` |Parent asset group in the hierarchy.|
|[Asset_Group_Code](#asset_group_code)|`nvarchar(20)` ||
|[Asset_Group_Name](#asset_group_name)|`nvarchar(254)` ||
|[Default_Valuation_Model_Id](#default_valuation_model_id)|`uniqueidentifier` |Default valuation model when creating new assets from this group|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Asset_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


