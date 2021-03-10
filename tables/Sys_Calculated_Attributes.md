# Table Sys_Calculated_Attributes

User-defined read-only calculated attribute. Entity: Sys_Calculated_Attributes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Repository_Name](#repository_name)|`nvarchar(128)` |The repository, for which the attribute is defined.|
|[Name](#name)|`nvarchar(128)` |The unique name of the attribute within the repository.|
|[Caption](#caption)|`nvarchar(512)` `ML`|The multi-language caption, used to display the attribute.|
|[Is_Active](#is_active)|`bit` |True if the attribute is activated and added to the repository.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Calculated_Attribute_Id](#calculated_attribute_id)|`uniqueidentifier` `PK`||
|[Starting_Expression_No](#starting_expression_no)|`int` |The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Repository_Name


Repository_Name


The repository, for which the attribute is defined.


The repository, for which the attribute is defined.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Repository_Name](Sys_Calculated_Attributes.md#repository_name)|
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
|Max Length|128|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Name


Name


The unique name of the attribute within the repository.


The unique name of the attribute within the repository.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Name](Sys_Calculated_Attributes.md#name)|
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
|Max Length|128|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Caption


Caption


The multi-language caption, used to display the attribute.


The multi-language caption, used to display the attribute.

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Caption](Sys_Calculated_Attributes.md#caption)|
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
|Max Length|512|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


True if the attribute is activated and added to the repository.


True if the attribute is activated and added to the repository.

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
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Is_Active](Sys_Calculated_Attributes.md#is_active)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Notes](Sys_Calculated_Attributes.md#notes)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Calculated_Attribute_Id


Calculated_Attribute_Id

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
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Calculated_Attribute_Id](Sys_Calculated_Attributes.md#calculated_attribute_id)|
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

### Starting_Expression_No


Starting_Expression_No


The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute.


The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|10|
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Starting_Expression_No](Sys_Calculated_Attributes.md#starting_expression_no)|
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
|Derived From|[Sys_Calculated_Attributes](Sys_Calculated_Attributes.md).[Row_Version](Sys_Calculated_Attributes.md#row_version)|
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


