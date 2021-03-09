# Table Eam_Maintenance_Type_Groups

Represents the hierarchy of the groups of maintenance types. Entity: Eam_Maintenance_Type_Groups (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Group_Code](#maintenance_type_group_code)|`nvarchar(16)` |Unique code of the group.|
|[Parent_Maintenance_Type_Group_Id](#parent_maintenance_type_group_id)|`uniqueidentifier` |Parent group. NULL denotes a root group.|
|[Maintenance_Type_Group_Name](#maintenance_type_group_name)|`nvarchar(254)` `ML`|Multilanguage name of the group.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parent_Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Group_Name

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


