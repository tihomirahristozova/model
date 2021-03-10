# Table Prj_Project_Tasks

Represents one task of a project. Entity: Prj_Project_Tasks

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` |The project, to which this task belongs.|
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` |The work element under which the task is filed.|
|[Task_Name](#task_name)|`nvarchar(254)` |The short name of the task. It is best practice to contain the target of the task.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource, which is required for the task. NULL means - do not plan any resource|
|[Start_Date_Time](#start_date_time)|`datetime` |The date and time when the task is planned to start.|
|[Finish_Date_Time](#finish_date_time)|`datetime` |The date and time when the task is planned to finish.|
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` |Type of work to be done. NULL means that type of work is undetermined yet.|
|[Planned_Duration_Hours](#planned_duration_hours)|`decimal(8, 2)` |Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time.|
|[Budget_Labor_Amount](#budget_labor_amount)|`decimal(12, 2)` |Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. NULL means that budgeting for the item is not calculated|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |The responsible party. Usually a person and usually one of the project participants. NULL means that responsible is not yet determined|
|[Activity_Id](#activity_id)|`uniqueidentifier` |The Id of the Cm_Activity created for this task. NULL means that activity is still not created|
|[Project_Task_No](#project_task_no)|`int` |Consecutive task number, unique within the project.|
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` |The type of the task. Determines the work type of the tasks, default billing rules, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Id


Project_Task_Id

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
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Project_Task_Id](Prj_Project_Tasks.md#project_task_id)|
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

### Project_Id


Project_Id


The project, to which this task belongs.


The project, to which this task belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Projects](Prj_Projects.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Project_Id](Prj_Project_Tasks.md#project_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Project_Work_Element_Id


Project_Work_Element_Id


The work element under which the task is filed.


The work element under which the task is filed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Project_Work_Elements](Prj_Project_Work_Elements.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Project_Work_Element_Id](Prj_Project_Tasks.md#project_work_element_id)|
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

### Task_Name


Task_Name


The short name of the task. It is best practice to contain the target of the task.


The short name of the task. It is best practice to contain the target of the task.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Task_Name](Prj_Project_Tasks.md#task_name)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

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
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Notes](Prj_Project_Tasks.md#notes)|
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
|UI Width|200|
|Supports EQUALS_IN|no|

### Resource_Id


Resource_Id


The resource, which is required for the task. NULL means - do not plan any resource


The resource, which is required for the task. NULL means - do not plan any resource

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Resources](Prj_Resources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Resource_Id](Prj_Project_Tasks.md#resource_id)|
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
|Equals|NULL|yes|no|

### Start_Date_Time


Start_Date_Time


The date and time when the task is planned to start.


The date and time when the task is planned to start.

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
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Start_Date_Time](Prj_Project_Tasks.md#start_date_time)|
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
|GreaterThanOrLessThan|None|no|no|

### Finish_Date_Time


Finish_Date_Time


The date and time when the task is planned to finish.


The date and time when the task is planned to finish.

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
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Finish_Date_Time](Prj_Project_Tasks.md#finish_date_time)|
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
|GreaterThanOrLessThan|None|no|no|

### Work_Type_Id


Work_Type_Id


Type of work to be done. NULL means that type of work is undetermined yet.


Type of work to be done. NULL means that type of work is undetermined yet.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Type_Work_Types](Prj_Type_Work_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Work_Type_Id](Prj_Project_Tasks.md#work_type_id)|
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
|Equals|NULL|yes|no|

### Planned_Duration_Hours


Planned_Duration_Hours


Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time.


Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time.

| Property | Value |
| - | - |
|Type|decimal(8, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Planned_Duration_Hours](Prj_Project_Tasks.md#planned_duration_hours)|
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

### Budget_Labor_Amount


Budget_Labor_Amount


Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. NULL means that budgeting for the item is not calculated


Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. NULL means that budgeting for the item is not calculated

| Property | Value |
| - | - |
|Type|decimal(12, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Budget_Labor_Amount](Prj_Project_Tasks.md#budget_labor_amount)|
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

### Responsible_Party_Id


Responsible_Party_Id


The responsible party. Usually a person and usually one of the project participants. NULL means that responsible is not yet determined


The responsible party. Usually a person and usually one of the project participants. NULL means that responsible is not yet determined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Responsible_Party_Id](Prj_Project_Tasks.md#responsible_party_id)|
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
|Equals|NULL|yes|no|

### Activity_Id


Activity_Id


The Id of the Cm_Activity created for this task. NULL means that activity is still not created


The Id of the Cm_Activity created for this task. NULL means that activity is still not created

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Activities](Cm_Activities.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Activity_Id](Prj_Project_Tasks.md#activity_id)|
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
|Equals|NULL|yes|no|

### Project_Task_No


Project_Task_No


Consecutive task number, unique within the project.


Consecutive task number, unique within the project.

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
|Autoincrement|10|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Project_Task_No](Prj_Project_Tasks.md#project_task_no)|
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

### Task_Type_Id


Task_Type_Id


The type of the task. Determines the work type of the tasks, default billing rules, etc.


The type of the task. Determines the work type of the tasks, default billing rules, etc.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Task_Types](Prj_Task_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Task_Type_Id](Prj_Project_Tasks.md#task_type_id)|
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
|Derived From|[Prj_Project_Tasks](Prj_Project_Tasks.md).[Row_Version](Prj_Project_Tasks.md#row_version)|
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


