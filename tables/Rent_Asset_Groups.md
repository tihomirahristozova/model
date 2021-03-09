# Table Rent_Asset_Groups

Groups the rentable assets in hierarchy of logical groups. Entity: Rent_Asset_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rental_Asset_Group_Id](#rental_asset_group_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Group_Code](#rental_asset_group_code)|`nvarchar(3)` |Asset group code, unique within the parent node.|
|[Rental_Asset_Group_Name](#rental_asset_group_name)|`nvarchar(254)` |Asset group name, unique within the parent node.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |The full path of the parent node.|
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rental_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Rental_Asset_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Parent_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


