# Table Eam_Managed_Assets

Contains the managed assets. The management of assets include maintenance planning and execution, location assignments tracking, etc. Entity: Eam_Managed_Assets (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which the managed asset belongs.|
|[Managed_Asset_Code](#managed_asset_code)|`nvarchar(16)` |Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company.|
|[Managed_Asset_Name](#managed_asset_name)|`nvarchar(254)` `ML`|Name of the managed asset (multi-language).|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The type of the asset. Determines the tracked parameters for the asset, the applicable maintenance types, etc.|
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` |The organizational group of the asset. Used for organizational purposes only.|
|[Registration_Number](#registration_number)|`nvarchar(32)` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Managed_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


