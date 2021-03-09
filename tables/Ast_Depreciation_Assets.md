# Table Ast_Depreciation_Assets

Depreciation document line. Can specify assets, whose depreciation should be calculated. Entity: Ast_Depreciation_Assets

## Owner Tables Hierarchy

* [Ast_Depreciations](Ast_Depreciations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Asset_Id](#depreciation_asset_id)|`uniqueidentifier` `PK`||
|[Depreciation_Id](#depreciation_id)|`uniqueidentifier` ||
|[Asset_Id](#asset_id)|`uniqueidentifier` |Specifies the asset, whose depreciation should be calculated with the current document.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


