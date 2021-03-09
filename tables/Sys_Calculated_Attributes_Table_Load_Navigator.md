# Query Sys_Calculated_Attributes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Calculated_Attribute_Id](#calculated_attribute_id)|`uniqueidentifier` `PK`||
|[Repository_Name](#repository_name)|`nvarchar` ||
|[Name](#name)|`nvarchar` |The unique name of the attribute within the repository.|
|[Caption](#caption)|`nvarchar` `ML`|The multi-language caption, used to display the attribute.|
|[Starting_Expression_No](#starting_expression_no)|`int` |The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute.|
|[Is_Active](#is_active)|`bit` |True if the attribute is activated and added to the repository.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Calculated_Attribute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Caption

| Property | Value |
| - | - |
|Type|nvarchar|

### Starting_Expression_No

| Property | Value |
| - | - |
|Type|int|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


