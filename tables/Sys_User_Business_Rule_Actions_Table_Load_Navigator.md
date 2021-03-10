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


User_Business_Rule_Action_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[User_Business_Rule_Action_Id](Sys_User_Business_Rule_Actions.md#user_business_rule_action_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### User_Business_Rule_Id


User_Business_Rule_Id


The business rule, for which the action is defined.


The business rule, for which the action is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_User_Business_Rules](Sys_User_Business_Rules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[User_Business_Rule_Id](Sys_User_Business_Rule_Actions.md#user_business_rule_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Action_No


Action_No


Consecutive number of the action, unique within the business rule.


Consecutive number of the action, unique within the business rule.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Action_No](Sys_User_Business_Rule_Actions.md#action_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Action_Type


Action_Type


Specifies the type of action to perform.


Specifies the type of action to perform.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Allowed Values|`SETVALUE`, `FAIL`, `SENDMAIL`, `WARNING`, `NOTIFYUSER`|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Action_Type](Sys_User_Business_Rule_Actions.md#action_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter1_Type


Parameter1_Type


The type of the parameter specifies how to obtain the parameter value.


The type of the parameter specifies how to obtain the parameter value.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter1_Type](Sys_User_Business_Rule_Actions.md#parameter1_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter1_Value


Parameter1_Value


The actual value of the parameter.


The actual value of the parameter.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter1_Value](Sys_User_Business_Rule_Actions.md#parameter1_value)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter2_Type


Parameter2_Type


The type of the parameter specifies how to obtain the parameter value.


The type of the parameter specifies how to obtain the parameter value.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter2_Type](Sys_User_Business_Rule_Actions.md#parameter2_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter2_Value


Parameter2_Value


The actual value of the parameter.


The actual value of the parameter.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter2_Value](Sys_User_Business_Rule_Actions.md#parameter2_value)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter3_Type


Parameter3_Type


The type of the parameter specifies how to obtain the parameter value.


The type of the parameter specifies how to obtain the parameter value.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `FMTSTR`|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter3_Type](Sys_User_Business_Rule_Actions.md#parameter3_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter3_Value


Parameter3_Value


The actual value of the parameter.


The actual value of the parameter.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Parameter3_Value](Sys_User_Business_Rule_Actions.md#parameter3_value)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Actions](Sys_User_Business_Rule_Actions.md).[Row_Version](Sys_User_Business_Rule_Actions.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


