# Table Inv_Store_Groups

Hierarchy of store groups. Entity: Inv_Store_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Group_Id](#store_group_id)|`uniqueidentifier` `PK`||
|[Store_Group_Name](#store_group_name)|`nvarchar(254)` `ML`||
|[Store_Group_Code](#store_group_code)|`nvarchar(16)` ||
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005.|
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Store_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Store_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parent_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


