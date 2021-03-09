# Table Sys_User_Business_Rule_Actions

Represents an action within a business rule. Entity: Sys_User_Business_Rule_Actions

## Owner Tables Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Action_No](#action_no)|`int` |Consecutive number of the action, unique within the business rule.|
|[Action_Type](#action_type)|`nvarchar(32)` Allowed: `SETVALUE`, `FAIL`, `SENDMAIL`, `WARNING`, `NOTIFYUSER`|Specifies the type of action to perform.|
|[Parameter1_Type](#parameter1_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter1_Value](#parameter1_value)|`nvarchar(256)` |The actual value of the parameter.|
|[Parameter2_Type](#parameter2_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter2_Value](#parameter2_value)|`nvarchar(256)` |The actual value of the parameter.|
|[Parameter3_Type](#parameter3_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter3_Value](#parameter3_value)|`nvarchar(256)` |The actual value of the parameter.|
|[User_Business_Rule_Action_Id](#user_business_rule_action_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The business rule, for which the action is defined.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Action_No

| Property | Value |
| - | - |
|Type|int|

### Action_Type

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Parameter1_Type

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parameter1_Value

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Parameter2_Type

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parameter2_Value

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Parameter3_Type

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parameter3_Value

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### User_Business_Rule_Action_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


