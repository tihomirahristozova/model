# Table Its_Commodity_Codes

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` `PK`||
|[Commodity_Code](#commodity_code)|`nvarchar(8)` |Product code from the Intrastat Combined nomenclature|
|[Description](#description)|`nvarchar(4000)` `ML`|Description of the product code from the Intrastat Combined nomenclature|
|[Supplementary_Unit](#supplementary_unit)|`nvarchar(16)` |If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations|
|[Valid_From](#valid_from)|`date` |The starting date of validity of this code.|
|[Valid_To](#valid_to)|`date` |The ending date of validity of this code.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Intrastat_Commodity_Code_Id


Intrastat_Commodity_Code_Id

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
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Intrastat_Commodity_Code_Id](Its_Commodity_Codes.md#intrastat_commodity_code_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Commodity_Code


Commodity_Code


Product code from the Intrastat Combined nomenclature


Product code from the Intrastat Combined nomenclature

| Property | Value |
| - | - |
|Type|nvarchar(8)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Commodity_Code](Its_Commodity_Codes.md#commodity_code)|
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
|Max Length|8|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Description


Description


Description of the product code from the Intrastat Combined nomenclature


Description of the product code from the Intrastat Combined nomenclature

| Property | Value |
| - | - |
|Type|nvarchar(4000)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Description](Its_Commodity_Codes.md#description)|
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
|Max Length|4000|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Supplementary_Unit


Supplementary_Unit


If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations


If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Supplementary_Unit](Its_Commodity_Codes.md#supplementary_unit)|
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
|Max Length|16|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Valid_From


Valid_From


The starting date of validity of this code.


The starting date of validity of this code.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Valid_From](Its_Commodity_Codes.md#valid_from)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Valid_To


Valid_To


The ending date of validity of this code.


The ending date of validity of this code.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Valid_To](Its_Commodity_Codes.md#valid_to)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

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
|Derived From|[Its_Commodity_Codes](Its_Commodity_Codes.md).[Row_Version](Its_Commodity_Codes.md#row_version)|
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


