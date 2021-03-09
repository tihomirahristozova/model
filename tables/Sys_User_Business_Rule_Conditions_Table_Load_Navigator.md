# Query Sys_User_Business_Rule_Conditions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Condition_Id](#user_business_rule_condition_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The business rule, for which the condition is defined.|
|[Condition_No](#condition_no)|`int` ||
|[Attribute_Name](#attribute_name)|`nvarchar` |The attribute, which will be tested.|
|[Comparison_Type](#comparison_type)|`nvarchar` Allowed: `Equals`, `Greater_Than`, `Less_Than`, `Like`, `IsNull`, `Not_Equals`||
|[Value](#value)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Notes](#notes)|`nvarchar` ||

## Columns

### User_Business_Rule_Condition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_No

| Property | Value |
| - | - |
|Type|int|

### Attribute_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Comparison_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


