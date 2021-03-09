# Query Eam_Managed_Assets_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Group_Notes](#group_notes)|`nvarchar` ||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which the managed asset belongs.|
|[Managed_Asset_Code](#managed_asset_code)|`nvarchar` |Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company.|
|[Managed_Asset_Name](#managed_asset_name)|`nvarchar` `ML`|Name of the managed asset (multi-language).|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The type of the asset. Determines the tracked parameters for the asset, the applicable maintenance types, etc.|
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` |The organizational group of the asset. Used for organizational purposes only.|
|[Registration_Number](#registration_number)|`nvarchar` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Notes](#notes)|`nvarchar` ||
|[Parent_Managed_Asset_Group_Id](#parent_managed_asset_group_id)|`uniqueidentifier` ||
|[Managed_Asset_Group_Code](#managed_asset_group_code)|`nvarchar` |Unique (within all groups) code of the asset group.|
|[Managed_Asset_Group_Name](#managed_asset_group_name)|`nvarchar` `ML`|Name of the asset group (multi-language).|

## Columns

### Group_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Managed_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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


