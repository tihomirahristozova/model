# Table Sys_Object_Versions

Contains history of saved version of the managed objects. Entity: Sys_Object_Versions

## Owner Tables Hierarchy

* [Sys_Objects](Sys_Objects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Version_Id](#object_version_id)|`uniqueidentifier` `PK`||
|[Object_Id](#object_id)|`uniqueidentifier` |The object, for which a version is stored.|
|[Version](#version)|`int` |The version number of the version, stored in the current row, starting from 1.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, which saved the version.|
|[Version_Time](#version_time)|`datetime` |The timestamp when the version was saved.|
|[Object_Contents](#object_contents)|`varbinary` |The compressed contents of the object.|
|[Version_Type](#version_type)|`nvarchar(1)` Allowed: `C`, `U`|Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object.|
|[Server_Version](#server_version)|`nvarchar(15)` |The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). NULL means the version is unknown.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Version_Id


Object_Version_Id

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
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Object_Version_Id](Sys_Object_Versions.md#object_version_id)|
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

### Object_Id


Object_Id


The object, for which a version is stored.


The object, for which a version is stored.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Objects](Sys_Objects.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Object_Id](Sys_Object_Versions.md#object_id)|
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

### Version


Version


The version number of the version, stored in the current row, starting from 1.


The version number of the version, stored in the current row, starting from 1.

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
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Version](Sys_Object_Versions.md#version)|
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
|GreaterThanOrLessThan|None|no|no|

### User_Id


User_Id


The user, which saved the version.


The user, which saved the version.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[User_Id](Sys_Object_Versions.md#user_id)|
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

### Version_Time


Version_Time


The timestamp when the version was saved.


The timestamp when the version was saved.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Version_Time](Sys_Object_Versions.md#version_time)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Object_Contents


Object_Contents


The compressed contents of the object.


The compressed contents of the object.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Object_Contents](Sys_Object_Versions.md#object_contents)|
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

### Version_Type


Version_Type


Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object.


Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object.

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
|Allowed Values|`C`, `U`|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Version_Type](Sys_Object_Versions.md#version_type)|
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

### Server_Version


Server_Version


The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). NULL means the version is unknown.


The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). NULL means the version is unknown.

| Property | Value |
| - | - |
|Type|nvarchar(15)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Server_Version](Sys_Object_Versions.md#server_version)|
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
|Max Length|15|
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
|Derived From|[Sys_Object_Versions](Sys_Object_Versions.md).[Row_Version](Sys_Object_Versions.md#row_version)|
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


