# Table Ast_Depreciation_Plan_Line_Fixed_Values

When specified, contains user-defined asset depreciation values for each depreciation period. Entity: Ast_Depreciation_Plan_Line_Fixed_Values

## Owner Tables Hierarchy

* [Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md)
* [Ast_Depreciation_Plans](Ast_Depreciation_Plans.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Plan_Line_Fixed_Value_Id](#depreciation_plan_line_fixed_value_id)|`uniqueidentifier` `PK`||
|[Depreciation_Plan_Line_Id](#depreciation_plan_line_id)|`uniqueidentifier` ||
|[Fixed_Value_Period_Month](#fixed_value_period_month)|`tinyint` |Month of the period for which the depreciation value is fixed|
|[Fixed_Value_Period_Year](#fixed_value_period_year)|`smallint` |Year of the period for which the depreciation value is fixed|
|[Depreciation_Value](#depreciation_value)|`decimal(14, 2)` |Fixed depreciation value for the period specified by Fixed_Value_Period_Month and Fixed_Value_Period_Year|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Plan_Line_Fixed_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Plan_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fixed_Value_Period_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Fixed_Value_Period_Year

| Property | Value |
| - | - |
|Type|smallint|

### Depreciation_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


