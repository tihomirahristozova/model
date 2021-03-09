# Table Eam_Managed_Asset_Types

Types of managed assets. Used to categorize the assets and the tracked parameters for each type. Entity: Eam_Managed_Asset_Types (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` `PK`|Types of Managed assets. Used to categorize the tracked parameters of the assets.|
|[Managed_Asset_Type_Code](#managed_asset_type_code)|`nvarchar(16)` |Unique code of the asset type.|
|[Managed_Asset_Type_Name](#managed_asset_type_name)|`nvarchar(254)` `ML`|Multilanguage name of the asset type.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the asset type is active for choosing in drop-down choices.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Managed_Asset_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


