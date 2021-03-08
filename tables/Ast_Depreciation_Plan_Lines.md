# Table Ast_Depreciation_Plan_Lines

Each record contains one depreciation plan for one valuation model of one asset. Entity: Ast_Depreciation_Plan_Lines

# Aggregate Hierarchy

* [Ast_Depreciation_Plans](Ast_Depreciation_Plans.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Depreciation_Plan_Line_Id|`Guid`|`PK`, Readonly||
|Depreciation_End_Date|`DateTime`||End date of the depreciation plan for this asset. `Required` |
|Depreciation_Start_Date|`DateTime`||Start date of the depreciation plan for this asset. `Required` |
|Line_No|`Int32`||Consecutive number of the line within the depreciation plan. `Required` `Filter(eq)` |
