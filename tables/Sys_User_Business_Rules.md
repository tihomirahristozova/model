# Table Sys_User_Business_Rules

Represents user-defined business rule. Entity: Sys_User_Business_Rules

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Code](#user_business_rule_code)|`nvarchar(16)` ||
|[User_Business_Rule_Name](#user_business_rule_name)|`nvarchar(254)` `ML`||
|[Repository_Name](#repository_name)|`nvarchar(128)` |The name of the repository, for which this business rule is defined.|
|[Layer](#layer)|`nvarchar(3)` Allowed: `FTE`, `BKE`, `COM`|Specifies in which layers the rule will be available. The available events and actions depend on the chosen layer.  Allowed values: FTE=Front-End, BKE=BackEnd, COM=Common (both).|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the rule is activated.|
|[Row_Version](#row_version)|`timestamp` ||
|[User_Startable](#user_startable)|`bit` |Specifies, that the rule can be manually started by the user.|
|[Icon](#icon)|`varbinary` |Visual icon of the rule in .PNG format.|
|[Script_Language](#script_language)|`nvarchar(16)` Allowed: `Integrated`, `CSharp`|The programming language used to define the rule actions.|
|[Script_Text](#script_text)|`nvarchar(2147483647)` |The program code used to define the rule actions.|

## Columns

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### User_Business_Rule_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Layer

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

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
|Type|nvarchar(16)|

### Script_Text

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


