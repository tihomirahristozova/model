# Table Cmm_Social_Groups

Represents a group of users, sharing interest in the group topic. Entity: Cmm_Social_Groups (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Social_Group_Id](#social_group_id)|`uniqueidentifier` `PK`||
|[Social_Group_Code](#social_group_code)|`nvarchar(32)` |Unique code of the group. Also used as group slug for Internet URL purposes.|
|[Social_Group_Name](#social_group_name)|`nvarchar(256)` |Multilanguage name of the group.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Social_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Social_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Social_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


