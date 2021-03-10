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


Intrastat_Commodity_Code_Id


The commodity code of the goods, according to the Intrastat commodity classification


The commodity code of the goods, according to the Intrastat commodity classification

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Its_Commodity_Codes](Its_Commodity_Codes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Intrastat_Commodity_Code_Id](Its_Declaration_Lines.md#intrastat_commodity_code_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Administrative_Region_Id


Administrative_Region_Id


Administrative region of the enterprise company at the time of the declaration


Administrative region of the enterprise company at the time of the declaration

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Administrative_Regions](Gen_Administrative_Regions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Administrative_Region_Id](Its_Declaration_Lines.md#administrative_region_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Intrastat_Declaration_Line_Id


Intrastat_Declaration_Line_Id


The unique id of the line


The unique id of the line

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

### Quantity_Supplementary_Unit


Quantity_Supplementary_Unit


Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified


Quantity of the goods in the supplementary unit. NULL when no supplementary unit is specified

| Property | Value |
| - | - |
|Type|decimal(10, 0)|
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

### Statistical_Value_Amount_Base


Statistical_Value_Amount_Base


Statistical value of the goods in the base currency


Statistical value of the goods in the base currency

| Property | Value |
| - | - |
|Type|decimal(10, 0)|
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

### Invoiced_Value_Amount_Base


Invoiced_Value_Amount_Base


Invoiced value of the goods in the base currency


Invoiced value of the goods in the base currency

| Property | Value |
| - | - |
|Type|decimal(10, 0)|
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

### Net_Mass_Kg


Net_Mass_Kg


Net mass of the goods in kg


Net mass of the goods in kg

| Property | Value |
| - | - |
|Type|decimal(14, 3)|
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

### Delivery_Terms


Delivery_Terms


Delivery terms - classification according to Intrastat (which uses the common abbreviations)


Delivery terms - classification according to Intrastat (which uses the common abbreviations)

| Property | Value |
| - | - |
|Type|nvarchar(3)|
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
|Max Length|3|
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
|Type|nvarchar(1)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Transaction_Nature


Transaction_Nature


Transaction nature, according to the Intrastat classification


Transaction nature, according to the Intrastat classification

| Property | Value |
| - | - |
|Type|nvarchar(2)|
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
|Max Length|2|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Transport_Country_Id


Transport_Country_Id


The country of the transportation company


The country of the transportation company

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Countries](Gen_Countries.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Transport_Country_Id](Its_Declaration_Lines.md#transport_country_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Party_Country_Id


Party_Country_Id


The country of the partner


The country of the partner

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Countries](Gen_Countries.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Party_Country_Id](Its_Declaration_Lines.md#party_country_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Origin_Country_Id


Origin_Country_Id


The country of origin of the goods. NULL for outbound declarations


The country of origin of the goods. NULL for outbound declarations

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Countries](Gen_Countries.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Origin_Country_Id](Its_Declaration_Lines.md#origin_country_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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

### Intrastat_Declaration_Id


Intrastat_Declaration_Id


The intrastat declaration, to which this line belongs


The intrastat declaration, to which this line belongs

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Its_Declarations](Its_Declarations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Intrastat_Declaration_Id](Its_Declaration_Lines.md#intrastat_declaration_id)|
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
|Equals|NULL|no|yes|

### Line_Action


Line_Action


Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted


Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted

| Property | Value |
| - | - |
|Type|nvarchar(3)|
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
|Max Length|3|
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
|Derived From|[Its_Declaration_Lines](Its_Declaration_Lines.md).[Row_Version](Its_Declaration_Lines.md#row_version)|
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


