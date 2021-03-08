# Table Ast_Depreciation_Methods

Depreciation methods. Contains both system-defined and user-defined methods. Entity: Ast_Depreciation_Methods

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Depreciation_Method_Id|`Guid`|`PK`, Readonly||
|Depreciation_Function|`DepreciationFunction`|Allowed: `FAC`, `STL`, `SYD`, `TAB`|Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table. `Required` `Default("STL")` |
|Factor|`Decimal`||Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor. `Required` `Default(1)` |
|Is_System|`Boolean`|Readonly|Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Months_In_A_Period|`Int32`||Number of equal valued months calculated with single application of the function. `Required` `Default(12)` |
|Depreciation_Method_Name|`String`||The name of this DepreciationMethod. `Required` `Filter(like)` |
|Period_Determination_Method|`PeriodDeterminationMethod`|Allowed: `NM`, `CM`, `BD`|Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days. `Required` |
|Start_From_Next_Month|`Boolean`|Readonly|When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month. `Required` `Default(true)` `ReadOnly` |
