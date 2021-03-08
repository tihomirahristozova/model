# Table Ast_Depreciation_Plan_Line_Fixed_Values

When specified, contains user-defined asset depreciation values for each depreciation period. Entity: Ast_Depreciation_Plan_Line_Fixed_Values

# Aggregate Hierarchy

* [Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md)
* [Ast_Depreciation_Plans](Ast_Depreciation_Plans.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Depreciation_Plan_Line_Fixed_Value_Id|`Guid`|`PK`, Readonly||
|Fixed_Value_Period_Month|`Byte`||Month of the period for which the depreciation value is fixed. `Required` |
|Fixed_Value_Period_Year|`Int16`||Year of the period for which the depreciation value is fixed. `Required` |
