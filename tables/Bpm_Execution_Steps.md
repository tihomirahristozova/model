# Table Bpm_Execution_Steps

Contains both historical and active steps in the execution of the business processes. Entity: Bpm_Execution_Steps

## Summary

| Name | Type | Description |
| - | - | --- |
|[Execution_Step_Id](#execution_step_id)|`uniqueidentifier` `PK`||
|[Process_Instance_Id](#process_instance_id)|`uniqueidentifier` |The process instance, which is being executed.|
|[Process_Element_Id](#process_element_id)|`uniqueidentifier` |The process element, which is being executed for the instance.|
|[Execution_State](#execution_state)|`int` |Shows where the execution of the step has reached. 0=Ready; 10=Active; 20=Executing; 30=Completing; 40=Failing; 50=Terminating; 60=Completed; 70=Failed; 80=Terminated.|
|[Start_Time](#start_time)|`datetime` |The date and time when the step execution started.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Execution_Step_Id


Execution_Step_Id

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
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Execution_Step_Id](Bpm_Execution_Steps.md#execution_step_id)|
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

### Process_Instance_Id


Process_Instance_Id


The process instance, which is being executed.


The process instance, which is being executed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Process_Instances](Bpm_Process_Instances.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Process_Instance_Id](Bpm_Execution_Steps.md#process_instance_id)|
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

### Process_Element_Id


Process_Element_Id


The process element, which is being executed for the instance.


The process element, which is being executed for the instance.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Process_Elements](Bpm_Process_Elements.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Process_Element_Id](Bpm_Execution_Steps.md#process_element_id)|
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

### Execution_State


Execution_State


Shows where the execution of the step has reached. 0=Ready; 10=Active; 20=Executing; 30=Completing; 40=Failing; 50=Terminating; 60=Completed; 70=Failed; 80=Terminated.


Shows where the execution of the step has reached. 0=Ready; 10=Active; 20=Executing; 30=Completing; 40=Failing; 50=Terminating; 60=Completed; 70=Failed; 80=Terminated.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Execution_State](Bpm_Execution_Steps.md#execution_state)|
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

### Start_Time


Start_Time


The date and time when the step execution started.


The date and time when the step execution started.

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
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Start_Time](Bpm_Execution_Steps.md#start_time)|
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
|Derived From|[Bpm_Execution_Steps](Bpm_Execution_Steps.md).[Row_Version](Bpm_Execution_Steps.md#row_version)|
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


