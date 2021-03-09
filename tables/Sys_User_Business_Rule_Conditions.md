# Table Sys_User_Business_Rule_Conditions

Represents one condition for the execution of a business rule. Entity: Sys_User_Business_Rule_Conditions

## Owner Tables Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The business rule, for which the condition is defined.|
|[Condition_No](#condition_no)|`int` |Unique consecutive number of the condition within the business rule.|
|[Attribute_Name](#attribute_name)|`nvarchar(64)` |The attribute, which will be tested.|
|[Comparison_Type](#comparison_type)|`nvarchar(16)` Allowed: `Equals`, `Greater_Than`, `Less_Than`, `Like`, `IsNull`, `Not_Equals`|How to compare the attribute and the value of the condition - e.g. Attribute-Comparison-Value.|
|[Value](#value)|`nvarchar(254)` |The value against which the data attribute will be tested.|
|[User_Business_Rule_Condition_Id](#user_business_rule_condition_id)|`uniqueidentifier` `PK`||
|[Row_Version](#row_version)|`timestamp` ||
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

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
|Type|nvarchar(64)|

### Comparison_Type

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### User_Business_Rule_Condition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


