# Query Sys_Calculated_Attribute_Expressions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Calculated_Attribute_Expression_Id](#calculated_attribute_expression_id)|`uniqueidentifier` `PK`||
|[Calculated_Attribute_Id](#calculated_attribute_id)|`uniqueidentifier` ||
|[Expression_No](#expression_no)|`int` |Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute.|
|[Operator](#operator)|`nvarchar` Allowed: `ADD`, `ADDDAYS`, `AND`, `CAST`, `CEILING`, `CONCAT`, `CONVERT`, `COUNT`, `DIVIDE`, `IN`, `IIF`, `INCNUM`, `EQUAL`, `FILTER`, `FIRST`, `FLOOR`, `FORMATSTRING`, `GETVALUE`, `GETOBJVALUE`, `GT`, `GTE`, `LIKE`, `LIST`, `LEFT`, `LEN`, `LT`, `LTE`, `MULTIPLY`, `NOT`, `OR`, `ORDERBY`, `POS`, `REGEX`, `REPLACE`, `RIGHT`, `ROUND`, `SELECT`, `SORT`, `SUBSTRING`, `SUM`, `TODAY`, `TOLOWER`, `TOP`, `TOUPPER`, `WHERE`|The exprssion operator. Available operators are limited to a pre-selected list of operators.|
|[Parameter1_Type](#parameter1_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter1_Value](#parameter1_value)|`nvarchar` |The actual value of parameter 1.|
|[Parameter2_Type](#parameter2_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter2_Value](#parameter2_value)|`nvarchar` |The actual value of the parameter.|
|[Parameter3_Type](#parameter3_type)|`nvarchar` Allowed: `CONST`, `ATTRIB`, `REF`, `CHILD`, `EXP`, `INPUT`, `REPO`, `SYS`|The type of the parameter specifies how to obtain the parameter value.|
|[Parameter3_Value](#parameter3_value)|`nvarchar` |The actual value of the parameter.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Calculated_Attribute_Expression_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calculated_Attribute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expression_No

| Property | Value |
| - | - |
|Type|int|

### Operator

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


