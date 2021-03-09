# Table Sys_Calculated_Attributes

User-defined read-only calculated attribute. Entity: Sys_Calculated_Attributes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Repository_Name](#repository_name)|`nvarchar(128)` |The repository, for which the attribute is defined.|
|[Name](#name)|`nvarchar(128)` |The unique name of the attribute within the repository.|
|[Caption](#caption)|`nvarchar(512)` `ML`|The multi-language caption, used to display the attribute.|
|[Is_Active](#is_active)|`bit` |True if the attribute is activated and added to the repository.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Calculated_Attribute_Id](#calculated_attribute_id)|`uniqueidentifier` `PK`||
|[Starting_Expression_No](#starting_expression_no)|`int` |The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Caption

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Calculated_Attribute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Expression_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


