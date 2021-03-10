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


Depreciation_Plan_Line_Fixed_Value_Id

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
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Depreciation_Plan_Line_Fixed_Value_Id](Ast_Depreciation_Plan_Line_Fixed_Values.md#depreciation_plan_line_fixed_value_id)|
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

### Depreciation_Plan_Line_Id


Depreciation_Plan_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Depreciation_Plan_Line_Id](Ast_Depreciation_Plan_Line_Fixed_Values.md#depreciation_plan_line_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Fixed_Value_Period_Month


Fixed_Value_Period_Month


Month of the period for which the depreciation value is fixed


Month of the period for which the depreciation value is fixed

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Fixed_Value_Period_Month](Ast_Depreciation_Plan_Line_Fixed_Values.md#fixed_value_period_month)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Fixed_Value_Period_Year


Fixed_Value_Period_Year


Year of the period for which the depreciation value is fixed


Year of the period for which the depreciation value is fixed

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Fixed_Value_Period_Year](Ast_Depreciation_Plan_Line_Fixed_Values.md#fixed_value_period_year)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Depreciation_Value


Depreciation_Value


Fixed depreciation value for the period specified by Fixed_Value_Period_Month and Fixed_Value_Period_Year


Fixed depreciation value for the period specified by Fixed_Value_Period_Month and Fixed_Value_Period_Year

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Depreciation_Value](Ast_Depreciation_Plan_Line_Fixed_Values.md#depreciation_value)|
|Format|N2|
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
|Order|2147483647|
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
|Derived From|[Ast_Depreciation_Plan_Line_Fixed_Values](Ast_Depreciation_Plan_Line_Fixed_Values.md).[Row_Version](Ast_Depreciation_Plan_Line_Fixed_Values.md#row_version)|
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


