# Table Sys_Calculated_Attribute_Expressions

Represent an expression within the calculation of a calculated attribute. Entity: Sys_Calculated_Attribute_Expressions

# Aggregate Hierarchy

* [Sys_Calculated_Attributes](Sys_Calculated_Attributes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Calculated_Attribute_Expression_Id|`Guid`|`PK`, Readonly||
|Expression_No|`Int32`||Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute. `Required` |
|Notes|`String`||Notes for this CalculatedAttributeExpression. |
|Operator|`ExpressionOperator`|Allowed: `ADD`, `ADDDAYS`, `AND`, `CAST`, `CEILING`, `CONCAT`, `CONVERT`, `COUNT`, `DIVIDE`, `IN`, `IIF`, `INCNUM`, `EQUAL`, `FILTER`, `FIRST`, `FLOOR`, `FORMATSTRING`, `GETVALUE`, `GETOBJVALUE`, `GT`, `GTE`, `LIKE`, `LIST`, `LEFT`, `LEN`, `LT`, `LTE`, `MULTIPLY`, `NOT`, `OR`, `ORDERBY`, `POS`, `REGEX`, `REPLACE`, `RIGHT`, `ROUND`, `SELECT`, `SORT`, `SUBSTRING`, `SUM`, `TODAY`, `TOLOWER`, `TOP`, `TOUPPER`, `WHERE`|The exprssion operator. Available operators are limited to a pre-selected list of operators. `Required` |
|Parameter1_Type|`ExpressionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter1_Value|`String`||The actual value of parameter 1. |
|Parameter2_Type|`ExpressionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter2_Value|`String`||The actual value of the parameter. |
|Parameter3_Type|`ExpressionParameterType?`|Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value. |
|Parameter3_Value|`String`||The actual value of the parameter. |
