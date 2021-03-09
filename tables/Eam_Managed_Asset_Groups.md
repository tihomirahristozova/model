# Table Eam_Managed_Asset_Groups

Organizational hierarchy of asset groups. Entity: Eam_Managed_Asset_Groups (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` `PK`||
|[Parent_Managed_Asset_Group_Id](#parent_managed_asset_group_id)|`uniqueidentifier` |The parent asset group in the hierarchy. NULL means this is a root group.|
|[Managed_Asset_Group_Code](#managed_asset_group_code)|`nvarchar(16)` |Unique (within all groups) code of the asset group.|
|[Managed_Asset_Group_Name](#managed_asset_group_name)|`nvarchar(254)` `ML`|Name of the asset group (multi-language).|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Managed_Asset_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


