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


Intrastat_Declaration_Line_Id

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
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Intrastat_Declaration_Line_Id](Its_Declaration_Lines.md#intrastat_declaration_line_id)|
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

### Line_No


Line_No


Consequtive line number within the intrastat declaration


Consequtive line number within the intrastat declaration

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|10|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Line_No](Its_Declaration_Lines.md#line_no)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Transaction_Nature


Transaction_Nature


Transaction nature, according to the Intrastat classification


Transaction nature, according to the Intrastat classification

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Transaction_Nature](Its_Declaration_Lines.md#transaction_nature)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Transport_Mode


Transport_Mode


Transportation mode - type of transportation used


Transportation mode - type of transportation used

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`, `7`, `8`, `9`|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Transport_Mode](Its_Declaration_Lines.md#transport_mode)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Delivery_Terms


Delivery_Terms


Delivery terms - classification according to Intrastat (which uses the common abbreviations)


Delivery terms - classification according to Intrastat (which uses the common abbreviations)

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Delivery_Terms](Its_Declaration_Lines.md#delivery_terms)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Net_Mass_Kg


Net_Mass_Kg


Net mass of the goods in kg


Net mass of the goods in kg

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Net_Mass_Kg](Its_Declaration_Lines.md#net_mass_kg)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Invoiced_Value_Amount_Base


Invoiced_Value_Amount_Base


Invoiced value of the goods in the base currency


Invoiced value of the goods in the base currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Invoiced_Value_Amount_Base](Its_Declaration_Lines.md#invoiced_value_amount_base)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Statistical_Value_Amount_Base


Statistical_Value_Amount_Base


Statistical value of the goods in the base currency


Statistical value of the goods in the base currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Statistical_Value_Amount_Base](Its_Declaration_Lines.md#statistical_value_amount_base)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Quantity_Supplementary_Unit


Quantity_Supplementary_Unit


Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified


Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Quantity_Supplementary_Unit](Its_Declaration_Lines.md#quantity_supplementary_unit)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Line_Action


Line_Action


Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted


Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`NEW`, `EDN`, `EDO`, `DEL`|
|Default Value|NEW|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Line_Action](Its_Declaration_Lines.md#line_action)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|


