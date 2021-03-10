# Table Sys_Audit_Log


## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Id](#object_id)|`uniqueidentifier` `PK`|The Id of the affected object|
|[Operation_System_User](#operation_system_user)|`nvarchar(256)` `PK`|Not used.|
|[Operation_Time](#operation_time)|`datetime` `PK`|Not used.|
|[Operation_Type](#operation_type)|`nvarchar(10)` `PK`|The type of operation - I=INSERT, D=DELETE, U=UPDATE|
|[Old_Values_XML](#old_values_xml)|`nvarchar(2147483647)` |Values of the document columns (without BLOBs) before the operation |
|[New_Values_XML](#new_values_xml)|`nvarchar(2147483647)` |The new values of the columns|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Id


Object_Id


The Id of the affected object


The Id of the affected object

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
|Default Value|None|
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Object_Id](Sys_Audit_Log.md#object_id)|
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

### Operation_System_User


Operation_System_User


Not used.


Not used.

| Property | Value |
| - | - |
|Type|nvarchar(256)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|2|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Operation_System_User](Sys_Audit_Log.md#operation_system_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
|Visible|yes|
|Max Length|256|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Operation_Time


Operation_Time


Not used.


Not used.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|3|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Operation_Time](Sys_Audit_Log.md#operation_time)|
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

### Operation_Type


Operation_Type


The type of operation - I=INSERT, D=DELETE, U=UPDATE


The type of operation - I=INSERT, D=DELETE, U=UPDATE

| Property | Value |
| - | - |
|Type|nvarchar(10)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|4|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Operation_Type](Sys_Audit_Log.md#operation_type)|
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
|Max Length|10|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Old_Values_XML


Old_Values_XML


Values of the document columns (without BLOBs) before the operation 


Values of the document columns (without BLOBs) before the operation 

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
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Old_Values_XML](Sys_Audit_Log.md#old_values_xml)|
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

### New_Values_XML


New_Values_XML


The new values of the columns


The new values of the columns

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
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[New_Values_XML](Sys_Audit_Log.md#new_values_xml)|
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
|Derived From|[Sys_Audit_Log](Sys_Audit_Log.md).[Row_Version](Sys_Audit_Log.md#row_version)|
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


