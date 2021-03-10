# Table Sys_Calculated_Attribute_Expressions

Represent an expression within the calculation of a calculated attribute. Entity: Sys_Calculated_Attribute_Expressions

## Owner Tables Hierarchy

* [Sys_Calculated_Attributes](Sys_Calculated_Attributes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Expression_No](#expression_no)|`int` |Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute.|
|[Operator](#operator)|`nvarchar(16)` Allowed: `ADD`, `ADDDAYS`, `AND`, `CAST`, `CEILING`, `CONCAT`, `CONVERT`, `COUNT`, `DIVIDE`, `IN`, `IIF`, `INCNUM`, `EQUAL`, `FILTER`, `FIRST`, `FLOOR`, `FORMATSTRING`, `GETVALUE`, `GETOBJVALUE`, `GT`, `GTE`, `LIKE`, `LIST`, `LEFT`, `LEN`, `LT`, `LTE`, `MULTIPLY`, `NOT`, `OR`, `ORDERBY`, `POS`, `REGEX`, `REPLACE`, `RIGHT`, `ROUND`, `SELECT`, `SORT`, `SUBSTRING`, `SUM`, `TODAY`, `TOLOWER`, `TOP`, `TOUPPER`, `WHERE`|The exprssion operator. Available operators are limited to a pre-selected list of operators.|
|[Parameter1_Type](#parameter1_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter1_Value](#parameter1_value)|`nvarchar(256)` |The actual value of parameter 1.|
|[Parameter2_Type](#parameter2_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter2_Value](#parameter2_value)|`nvarchar(256)` |The actual value of the parameter.|
|[Parameter3_Type](#parameter3_type)|`nvarchar(16)` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter3_Value](#parameter3_value)|`nvarchar(256)` |The actual value of the parameter.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Calculated_Attribute_Expression_Id](#calculated_attribute_expression_id)|`uniqueidentifier` `PK`||
|[Calculated_Attribute_Id](#calculated_attribute_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Expression_No


Expression_No


Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute.


Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute.

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
|Autoincrement|10|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Expression_No](Sys_Calculated_Attribute_Expressions.md#expression_no)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Operator


Operator


The exprssion operator. Available operators are limited to a pre-selected list of operators.


The exprssion operator. Available operators are limited to a pre-selected list of operators.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`ADD`, `ADDDAYS`, `AND`, `CAST`, `CEILING`, `CONCAT`, `CONVERT`, `COUNT`, `DIVIDE`, `IN`, `IIF`, `INCNUM`, `EQUAL`, `FILTER`, `FIRST`, `FLOOR`, `FORMATSTRING`, `GETVALUE`, `GETOBJVALUE`, `GT`, `GTE`, `LIKE`, `LIST`, `LEFT`, `LEN`, `LT`, `LTE`, `MULTIPLY`, `NOT`, `OR`, `ORDERBY`, `POS`, `REGEX`, `REPLACE`, `RIGHT`, `ROUND`, `SELECT`, `SORT`, `SUBSTRING`, `SUM`, `TODAY`, `TOLOWER`, `TOP`, `TOUPPER`, `WHERE`|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Operator](Sys_Calculated_Attribute_Expressions.md#operator)|
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
|Max Length|16|
|Order|4|
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
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter1_Type](Sys_Calculated_Attribute_Expressions.md#parameter1_type)|
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
|Max Length|16|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parameter1_Value


Parameter1_Value


The actual value of parameter 1.


The actual value of parameter 1.

| Property | Value |
| - | - |
|Type|nvarchar(256)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter1_Value](Sys_Calculated_Attribute_Expressions.md#parameter1_value)|
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
|Max Length|256|
|Order|7|
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
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter2_Type](Sys_Calculated_Attribute_Expressions.md#parameter2_type)|
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
|Max Length|16|
|Order|8|
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
|Type|nvarchar(256)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter2_Value](Sys_Calculated_Attribute_Expressions.md#parameter2_value)|
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
|Max Length|256|
|Order|10|
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
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter3_Type](Sys_Calculated_Attribute_Expressions.md#parameter3_type)|
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
|Max Length|16|
|Order|11|
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
|Type|nvarchar(256)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Parameter3_Value](Sys_Calculated_Attribute_Expressions.md#parameter3_value)|
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
|Max Length|256|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Notes](Sys_Calculated_Attribute_Expressions.md#notes)|
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
|Max Length|2147483647|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Calculated_Attribute_Expression_Id


Calculated_Attribute_Expression_Id

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
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Calculated_Attribute_Expression_Id](Sys_Calculated_Attribute_Expressions.md#calculated_attribute_expression_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Calculated_Attribute_Id


Calculated_Attribute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Calculated_Attribute_Id](Sys_Calculated_Attribute_Expressions.md#calculated_attribute_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Sys_Calculated_Attribute_Expressions](Sys_Calculated_Attribute_Expressions.md).[Row_Version](Sys_Calculated_Attribute_Expressions.md#row_version)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


