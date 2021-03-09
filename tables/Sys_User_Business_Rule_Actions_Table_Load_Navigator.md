# Query Sys_User_Business_Rule_Actions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Action_Id](#user_business_rule_action_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The business rule, for which the action is defined.|
|[Action_No](#action_no)|`int` |Consecutive number of the action, unique within the business rule.|
|[Action_Type](#action_type)|`nvarchar` Allowed: `SETVALUE`, `FAIL`, `SENDMAIL`, `WARNING`, `NOTIFYUSER`|Specifies the type of action to perform.|
|[Parameter1_Type](#parameter1_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter1_Value](#parameter1_value)|`nvarchar` |The actual value of the parameter.|
|[Parameter2_Type](#parameter2_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter2_Value](#parameter2_value)|`nvarchar` |The actual value of the parameter.|
|[Parameter3_Type](#parameter3_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter3_Value](#parameter3_value)|`nvarchar` |The actual value of the parameter.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### User_Business_Rule_Action_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Action_No

| Property | Value |
| - | - |
|Type|int|

### Action_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter1_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter1_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter2_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter2_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter3_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter3_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


