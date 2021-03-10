# Table Gen_Measurement_Units

Contains all measurement units, grouped in categories. Each category has one base unit (with ratio 1/1) and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Units

## Owner Tables Hierarchy

* [Gen_Measurement_Categories](Gen_Measurement_Categories.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique measurement unit Id|
|[Measurement_Category_Id](#measurement_category_id)|`uniqueidentifier` |Base measurement category Id|
|[Measurement_Unit_Name](#measurement_unit_name)|`nvarchar(64)` `ML`|Name of the measurement unit|
|[Multiplier](#multiplier)|`decimal(9, 3)` |Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base)|
|[Divisor](#divisor)|`decimal(9, 3)` |Divisor of the relative value of the measurement unit against other units (divisor when converting to base)|
|[Is_Default_Unit](#is_default_unit)|`bit` |1 if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category|
|[System_Unit](#system_unit)|`nvarchar(1)` Allowed: `G`, `H`, `L`, `N`, `P`, `V`, `W`, `T`|Not NULL only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH|
|[Measurement_Unit_Code](#measurement_unit_code)|`nvarchar(16)` |When not null, contains unique measurement unit code.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|Full multi-language description of the measurement unit.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id


Unique measurement unit Id


Unique measurement unit Id

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
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Id](Gen_Measurement_Units.md#id)|
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

### Measurement_Category_Id


Measurement_Category_Id


Base measurement category Id


Base measurement category Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Measurement_Categories](Gen_Measurement_Categories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Measurement_Category_Id](Gen_Measurement_Units.md#measurement_category_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Measurement_Unit_Name


Measurement_Unit_Name


Name of the measurement unit


Name of the measurement unit

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Measurement_Unit_Name](Gen_Measurement_Units.md#measurement_unit_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Multiplier


Multiplier


Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base)


Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base)

| Property | Value |
| - | - |
|Type|decimal(9, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Multiplier](Gen_Measurement_Units.md#multiplier)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Divisor


Divisor


Divisor of the relative value of the measurement unit against other units (divisor when converting to base)


Divisor of the relative value of the measurement unit against other units (divisor when converting to base)

| Property | Value |
| - | - |
|Type|decimal(9, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Divisor](Gen_Measurement_Units.md#divisor)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Is_Default_Unit


Is_Default_Unit


1 if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category


1 if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Is_Default_Unit](Gen_Measurement_Units.md#is_default_unit)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### System_Unit


System_Unit


Not NULL only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH


Not NULL only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`G`, `H`, `L`, `N`, `P`, `V`, `W`, `T`|
|Default Value|None|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[System_Unit](Gen_Measurement_Units.md#system_unit)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Measurement_Unit_Code


Measurement_Unit_Code


When not null, contains unique measurement unit code.


When not null, contains unique measurement unit code.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Measurement_Unit_Code](Gen_Measurement_Units.md#measurement_unit_code)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Description


Description


Full multi-language description of the measurement unit.


Full multi-language description of the measurement unit.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Description](Gen_Measurement_Units.md#description)|
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
|Max Length|2147483647|
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
|Derived From|[Gen_Measurement_Units](Gen_Measurement_Units.md).[Row_Version](Gen_Measurement_Units.md#row_version)|
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


