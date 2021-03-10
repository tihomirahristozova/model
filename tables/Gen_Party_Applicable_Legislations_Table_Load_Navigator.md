# Query Gen_Party_Applicable_Legislations_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Applicable_Legislation_Id](#party_applicable_legislation_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Applicable_Legislation](#applicable_legislation)|`nvarchar` Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Applicable_Legislation_Id


Party_Applicable_Legislation_Id

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
|Derived From|[Gen_Party_Applicable_Legislations](Gen_Party_Applicable_Legislations.md).[Party_Applicable_Legislation_Id](Gen_Party_Applicable_Legislations.md#party_applicable_legislation_id)|
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

### Party_Id


Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Party_Applicable_Legislations](Gen_Party_Applicable_Legislations.md).[Party_Id](Gen_Party_Applicable_Legislations.md#party_id)|
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
|Equals|NULL|no|no|

### Applicable_Legislation


Applicable_Legislation


A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc.


A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc.

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
|Allowed Values|`AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|
|Default Value|None|
|Derived From|[Gen_Party_Applicable_Legislations](Gen_Party_Applicable_Legislations.md).[Applicable_Legislation](Gen_Party_Applicable_Legislations.md#applicable_legislation)|
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
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Party_Applicable_Legislations](Gen_Party_Applicable_Legislations.md).[Notes](Gen_Party_Applicable_Legislations.md#notes)|
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
|Like|None|no|no|

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
|Derived From|[Gen_Party_Applicable_Legislations](Gen_Party_Applicable_Legislations.md).[Row_Version](Gen_Party_Applicable_Legislations.md#row_version)|
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


