# Query Sys_User_Business_Rules_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Code](#user_business_rule_code)|`nvarchar` ||
|[User_Business_Rule_Name](#user_business_rule_name)|`nvarchar` `ML`||
|[Repository_Name](#repository_name)|`nvarchar` |The name of the repository, for which this business rule is defined.|
|[Layer](#layer)|`nvarchar` Allowed: `FTE`, `BKE`, `COM`||
|[Notes](#notes)|`nvarchar` ||
|[Is_Active](#is_active)|`bit` ||
|[Row_Version](#row_version)|`timestamp` ||
|[User_Startable](#user_startable)|`bit` |Specifies, that the rule can be manually started by the user.|
|[Icon](#icon)|`varbinary` |Visual icon of the rule in .PNG format.|
|[Script_Language](#script_language)|`nvarchar` Allowed: `Integrated`, `CSharp`|The programming language used to define the rule actions.|
|[Script_Text](#script_text)|`nvarchar` |The program code used to define the rule actions.|

## Columns

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Business_Rule_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Layer

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### User_Startable

| Property | Value |
| - | - |
|Type|bit|

### Icon

| Property | Value |
| - | - |
|Type|varbinary|

### Script_Language

| Property | Value |
| - | - |
|Type|nvarchar|

### Script_Text

| Property | Value |
| - | - |
|Type|nvarchar|


