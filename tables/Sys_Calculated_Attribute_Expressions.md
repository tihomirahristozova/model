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

| Property | Value |
| - | - |
|Type|int|

### Operator

| Property | Value |
| - | - |
|Type|nvarchar(16)|

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Calculated_Attribute_Expression_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calculated_Attribute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


