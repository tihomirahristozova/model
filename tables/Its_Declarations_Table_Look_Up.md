# Query Its_Declarations_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Reference_Year](#reference_year)|`smallint` |Year, for which the declaration is prepared|
|[Reference_Month](#reference_month)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`|Month, for which the declaration is prepared|
|[Goods_Flow_Direction](#goods_flow_direction)|`nvarchar` Allowed: `A`, `D`|The flow direction of the goods. A=Arrival, D=Dispatch|
|[Declaration_Function](#declaration_function)|`nvarchar` Allowed: `R`, `C`|Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective|
|[Declare_Statistical_Values](#declare_statistical_values)|`bit` |Does the declaration contain statistical values? 1=Yes; 0=No|
|[Intrastat_Declaration_Id](#intrastat_declaration_id)|`uniqueidentifier` `PK`||

## Columns

### Reference_Year

| Property | Value |
| - | - |
|Type|smallint|

### Reference_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Goods_Flow_Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaration_Function

| Property | Value |
| - | - |
|Type|nvarchar|

### Declare_Statistical_Values

| Property | Value |
| - | - |
|Type|bit|

### Intrastat_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


