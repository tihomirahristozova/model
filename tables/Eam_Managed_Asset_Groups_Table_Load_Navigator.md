# Query Eam_Managed_Asset_Groups_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` `PK`||
|[Parent_Managed_Asset_Group_Id](#parent_managed_asset_group_id)|`uniqueidentifier` |The parent asset group in the hierarchy. NULL means this is a root group.|
|[Managed_Asset_Group_Code](#managed_asset_group_code)|`nvarchar` |Unique (within all groups) code of the asset group.|
|[Managed_Asset_Group_Name](#managed_asset_group_name)|`nvarchar` `ML`|Name of the asset group (multi-language).|
|[Notes](#notes)|`nvarchar` ||
|[Parent_Parent_Managed_Asset_Group_Id](#parent_parent_managed_asset_group_id)|`uniqueidentifier` |The parent asset group in the hierarchy. NULL means this is a root group.|
|[Parent_Managed_Asset_Group_Code](#parent_managed_asset_group_code)|`nvarchar` ||
|[Parent_Managed_Asset_Group_Name](#parent_managed_asset_group_name)|`nvarchar` `ML`||
|[Parent_Notes](#parent_notes)|`nvarchar` ||

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
|Type|nvarchar|

### Managed_Asset_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Parent_Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Managed_Asset_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Managed_Asset_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Notes

| Property | Value |
| - | - |
|Type|nvarchar|


