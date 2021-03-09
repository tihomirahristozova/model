# Query Ast_Depreciation_Methods_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` `PK`||
|[Depreciation_Method_Name](#depreciation_method_name)|`nvarchar` ||
|[Depreciation_Function](#depreciation_function)|`nvarchar` Allowed: `FAC`, `STL`, `SYD`, `TAB`||
|[Factor](#factor)|`decimal(0, 0)` ||
|[Months_In_A_Period](#months_in_a_period)|`int` ||
|[Start_From_Next_Month](#start_from_next_month)|`bit` ||
|[Is_System](#is_system)|`bit` Readonly||
|[Period_Determination_Method](#period_determination_method)|`nvarchar` Allowed: `NM`, `CM`, `BD`||

## Columns

### Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Method_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Depreciation_Function

| Property | Value |
| - | - |
|Type|nvarchar|

### Factor

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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
|Type|nvarchar|


