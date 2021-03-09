# Table Its_Declaration_Lines

Contains the details of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declaration_Lines

## Owner Tables Hierarchy

* [Its_Declarations](Its_Declarations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` |The commodity code of the goods, according to the Intrastat commodity classification|
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` |Administrative region of the enterprise company at the time of the declaration|
|[Intrastat_Declaration_Line_Id](#intrastat_declaration_line_id)|`uniqueidentifier` `PK`|The unique id of the line|
|[Quantity_Supplementary_Unit](#quantity_supplementary_unit)|`decimal(10, 0)` |Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified|
|[Statistical_Value_Amount_Base](#statistical_value_amount_base)|`decimal(10, 0)` |Statistical value of the goods in the base currency|
|[Invoiced_Value_Amount_Base](#invoiced_value_amount_base)|`decimal(10, 0)` |Invoiced value of the goods in the base currency|
|[Net_Mass_Kg](#net_mass_kg)|`decimal(14, 3)` |Net mass of the goods in kg|
|[Delivery_Terms](#delivery_terms)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Delivery terms - classification according to Intrastat (which uses the common abbreviations)|
|[Transport_Mode](#transport_mode)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `7`, `8`, `9`|Transportation mode - type of transportation used|
|[Transaction_Nature](#transaction_nature)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature, according to the Intrastat classification|
|[Transport_Country_Id](#transport_country_id)|`uniqueidentifier` |The country of the transportation company|
|[Party_Country_Id](#party_country_id)|`uniqueidentifier` |The country of the partner|
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |The country of origin of the goods. NULL for outbound declarations|
|[Line_No](#line_no)|`int` |Consequtive line number within the intrastat declaration|
|[Intrastat_Declaration_Id](#intrastat_declaration_id)|`uniqueidentifier` |The intrastat declaration, to which this line belongs|
|[Line_Action](#line_action)|`nvarchar(3)` Allowed: `NEW`, `EDN`, `EDO`, `DEL`|Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Intrastat_Commodity_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Declaration_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Supplementary_Unit

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Statistical_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Invoiced_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Net_Mass_Kg

| Property | Value |
| - | - |
|Type|decimal(14, 3)|

### Delivery_Terms

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Transport_Mode

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Transaction_Nature

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Origin_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Intrastat_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Action

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


