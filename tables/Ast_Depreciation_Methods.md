# Table Ast_Depreciation_Methods

Depreciation methods. Contains both system-defined and user-defined methods. Entity: Ast_Depreciation_Methods

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` `PK`||
|[Depreciation_Method_Name](#depreciation_method_name)|`nvarchar(254)` ||
|[Depreciation_Function](#depreciation_function)|`nvarchar(3)` Allowed: `FAC`, `STL`, `SYD`, `TAB`|Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table|
|[Factor](#factor)|`decimal(5, 3)` |Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor|
|[Months_In_A_Period](#months_in_a_period)|`int` |Number of equal valued months calculated with single application of the function|
|[Start_From_Next_Month](#start_from_next_month)|`bit` |When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month.|
|[Is_System](#is_system)|`bit` Readonly|Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user.|
|[Period_Determination_Method](#period_determination_method)|`nvarchar(2)` Allowed: `NM`, `CM`, `BD`|Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Method_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Depreciation_Function

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Factor

| Property | Value |
| - | - |
|Type|decimal(5, 3)|

### Months_In_A_Period

| Property | Value |
| - | - |
|Type|int|

### Start_From_Next_Month

| Property | Value |
| - | - |
|Type|bit|

### Is_System

| Property | Value |
| - | - |
|Type|bit|

### Period_Determination_Method

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


