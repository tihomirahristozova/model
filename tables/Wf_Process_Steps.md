# Table Wf_Process_Steps


## Owner Tables Hierarchy

* [Wf_Processes](Wf_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Step_Id](#process_step_id)|`uniqueidentifier` `PK`|Unique process step Id|
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this step belongs|
|[Step_Code](#step_code)|`nvarchar(6)` |Unique code of the step. Used to sort the steps for display purposes|
|[Step_Type](#step_type)|`nvarchar(3)` |Step type. STU=Start step (by user action); STE=Start step - by email; END=Ending step; ACT=User action; CHO=Choice|
|[Short_Title](#short_title)|`nvarchar(128)` |Very short multilanguage title, displayed on the process diagram. The user text should be 15-20 chars, for each language|
|[Role_Id](#role_id)|`uniqueidentifier` |The role responsible for execution of the step|
|[Instructions](#instructions)|`nvarchar(2147483647)` |Full decription and instructions for the step. Displayed to user when executing the step|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Step_Id


Process_Step_Id


Unique process step Id


Unique process step Id

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
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Process_Step_Id](Wf_Process_Steps.md#process_step_id)|
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

### Process_Id


Process_Id


The process, to which this step belongs


The process, to which this step belongs

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Wf_Processes](Wf_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Process_Id](Wf_Process_Steps.md#process_id)|
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

### Step_Code


Step_Code


Unique code of the step. Used to sort the steps for display purposes


Unique code of the step. Used to sort the steps for display purposes

| Property | Value |
| - | - |
|Type|nvarchar(6)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Step_Code](Wf_Process_Steps.md#step_code)|
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
|Max Length|6|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Step_Type


Step_Type


Step type. STU=Start step (by user action); STE=Start step - by email; END=Ending step; ACT=User action; CHO=Choice


Step type. STU=Start step (by user action); STE=Start step - by email; END=Ending step; ACT=User action; CHO=Choice

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
|Default Value|None|
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Step_Type](Wf_Process_Steps.md#step_type)|
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

### Short_Title


Short_Title


Very short multilanguage title, displayed on the process diagram. The user text should be 15-20 chars, for each language


Very short multilanguage title, displayed on the process diagram. The user text should be 15-20 chars, for each language

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Short_Title](Wf_Process_Steps.md#short_title)|
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

### Role_Id


Role_Id


The role responsible for execution of the step


The role responsible for execution of the step

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Roles](Wf_Roles.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Role_Id](Wf_Process_Steps.md#role_id)|
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

### Instructions


Instructions


Full decription and instructions for the step. Displayed to user when executing the step


Full decription and instructions for the step. Displayed to user when executing the step

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
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Instructions](Wf_Process_Steps.md#instructions)|
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
|Derived From|[Wf_Process_Steps](Wf_Process_Steps.md).[Row_Version](Wf_Process_Steps.md#row_version)|
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


