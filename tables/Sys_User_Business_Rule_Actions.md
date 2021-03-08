# Table Sys_User_Business_Rule_Actions

Represents an action within a business rule. Entity: Sys_User_Business_Rule_Actions

# Aggregate Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Business_Rule_Action_Id|`Guid`|`PK`, Readonly||
|Action_No|`Int32`||Consecutive number of the action, unique within the business rule. `Required` |
|Action_Type|`ActionType`|Allowed: `SETVALUE`, `FAIL`, `SENDMAIL`, `WARNING`, `NOTIFYUSER`|Specifies the type of action to perform. `Required` |
|Parameter1_Type|`ActionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter1_Value|`String`||The actual value of the parameter. |
|Parameter2_Type|`ActionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter2_Value|`String`||The actual value of the parameter. |
|Parameter3_Type|`ActionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter3_Value|`String`||The actual value of the parameter. |
