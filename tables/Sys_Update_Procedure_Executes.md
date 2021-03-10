# Table Sys_Update_Procedure_Executes

Contains data about the execution of Upgrade Procedures. Contains status messages and ensures that each procedure is executed only once. Entity: Sys_Update_Procedure_Executes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Update_Procedure_Execute_Id](#update_procedure_execute_id)|`uniqueidentifier` `PK`||
|[Update_Procedure](#update_procedure)|`nvarchar(128)` |The system name of the executed update procedure.|
|[Execute_Time](#execute_time)|`datetime` |The time, when the update procedure was executed.|
|[Successful](#successful)|`bit` |True when the execution was successfull.|
|[Result_Message](#result_message)|`nvarchar(1024)` |Error or success message|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Update_Procedure_Execute_Id


Update_Procedure_Execute_Id

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
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Update_Procedure_Execute_Id](Sys_Update_Procedure_Executes.md#update_procedure_execute_id)|
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

### Update_Procedure


Update_Procedure


The system name of the executed update procedure.


The system name of the executed update procedure.

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
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Update_Procedure](Sys_Update_Procedure_Executes.md#update_procedure)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Execute_Time


Execute_Time


The time, when the update procedure was executed.


The time, when the update procedure was executed.

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
|Default Value|CurrentDateTime|
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Execute_Time](Sys_Update_Procedure_Executes.md#execute_time)|
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

### Successful


Successful


True when the execution was successfull.


True when the execution was successfull.

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
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Successful](Sys_Update_Procedure_Executes.md#successful)|
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

### Result_Message


Result_Message


Error or success message


Error or success message

| Property | Value |
| - | - |
|Type|nvarchar(1024)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Result_Message](Sys_Update_Procedure_Executes.md#result_message)|
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
|Max Length|1024|
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
|Derived From|[Sys_Update_Procedure_Executes](Sys_Update_Procedure_Executes.md).[Row_Version](Sys_Update_Procedure_Executes.md#row_version)|
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


