# Query Its_Declaration_Lines_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Intrastat_Declaration_Line_Id](#intrastat_declaration_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` |Consequtive line number within the intrastat declaration|
|[Transaction_Nature](#transaction_nature)|`nvarchar` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature, according to the Intrastat classification|
|[Transport_Mode](#transport_mode)|`nvarchar` Allowed: `1`, `2`, `3`, `4`, `5`, `7`, `8`, `9`|Transportation mode - type of transportation used|
|[Delivery_Terms](#delivery_terms)|`nvarchar` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Delivery terms - classification according to Intrastat (which uses the common abbreviations)|
|[Net_Mass_Kg](#net_mass_kg)|`decimal(0, 0)` |Net mass of the goods in kg|
|[Invoiced_Value_Amount_Base](#invoiced_value_amount_base)|`decimal(0, 0)` |Invoiced value of the goods in the base currency|
|[Statistical_Value_Amount_Base](#statistical_value_amount_base)|`decimal(0, 0)` |Statistical value of the goods in the base currency|
|[Quantity_Supplementary_Unit](#quantity_supplementary_unit)|`decimal(0, 0)` |Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified|
|[Line_Action](#line_action)|`nvarchar` Allowed: `NEW`, `EDN`, `EDO`, `DEL`|Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted|

## Columns

### Intrastat_Declaration_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Transaction_Nature

| Property | Value |
| - | - |
|Type|nvarchar|

### Transport_Mode

| Property | Value |
| - | - |
|Type|nvarchar|

### Delivery_Terms

| Property | Value |
| - | - |
|Type|nvarchar|

### Net_Mass_Kg

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Statistical_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Supplementary_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Action

| Property | Value |
| - | - |
|Type|nvarchar|


