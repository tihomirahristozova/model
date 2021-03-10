# Table Sys_Translations

Contains user-defined translations for non-english languages of the user interface and program messages. Entity: Sys_Translations

## Summary

| Name | Type | Description |
| - | - | --- |
|[Translation_Id](#translation_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(50)` |The application, containing the resource. For base resource types (T,C,H), this is NULL|
|[Language](#language)|`nvarchar(8)` |The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us"|
|[Resource_Type](#resource_type)|`nvarchar(1)` Allowed: `T`, `C`, `H`, `R`, `E`, `M`, `S`|T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String|
|[Resource_Id](#resource_id)|`nvarchar(800)` |The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code|
|[Translation](#translation)|`nvarchar(2147483647)` |The translated text|
|[Creation_Time](#creation_time)|`datetime` Readonly|Timestamp when the translation was first created|
|[Update_Time](#update_time)|`datetime` Readonly|When the translation was last updated|
|[Active](#active)|`bit` |True when the translation is verified and activated.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Translation_Id


Translation_Id

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
|Derived From|[Sys_Translations](Sys_Translations.md).[Translation_Id](Sys_Translations.md#translation_id)|
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

### Application_Name


Application_Name


The application, containing the resource. For base resource types (T,C,H), this is NULL


The application, containing the resource. For base resource types (T,C,H), this is NULL

| Property | Value |
| - | - |
|Type|nvarchar(50)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Translations](Sys_Translations.md).[Application_Name](Sys_Translations.md#application_name)|
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
|Max Length|50|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Language


Language


The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us"


The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us"

| Property | Value |
| - | - |
|Type|nvarchar(8)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|en|
|Derived From|[Sys_Translations](Sys_Translations.md).[Language](Sys_Translations.md#language)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Type


Resource_Type


T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String


T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String

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
|Allowed Values|`T`, `C`, `H`, `R`, `E`, `M`, `S`|
|Default Value|S|
|Derived From|[Sys_Translations](Sys_Translations.md).[Resource_Type](Sys_Translations.md#resource_type)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Id


Resource_Id


The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code


The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code

| Property | Value |
| - | - |
|Type|nvarchar(800)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Translations](Sys_Translations.md).[Resource_Id](Sys_Translations.md#resource_id)|
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
|Max Length|800|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Translation


Translation


The translated text


The translated text

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Translations](Sys_Translations.md).[Translation](Sys_Translations.md#translation)|
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

### Creation_Time


Creation_Time


Timestamp when the translation was first created


Timestamp when the translation was first created

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Sys_Translations](Sys_Translations.md).[Creation_Time](Sys_Translations.md#creation_time)|
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
|GreaterThanOrLessThan|None|no|yes|

### Update_Time


Update_Time


When the translation was last updated


When the translation was last updated

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Sys_Translations](Sys_Translations.md).[Update_Time](Sys_Translations.md#update_time)|
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

### Active


Active


True when the translation is verified and activated.


True when the translation is verified and activated.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Sys_Translations](Sys_Translations.md).[Active](Sys_Translations.md#active)|
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
|Equals|NULL|no|no|

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
|Derived From|[Sys_Translations](Sys_Translations.md).[Row_Version](Sys_Translations.md#row_version)|
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


