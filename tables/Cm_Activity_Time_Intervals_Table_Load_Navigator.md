# Query Cm_Activity_Time_Intervals_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Id](#document_id)|`uniqueidentifier` |The task's document (for entry date, task type, status)|
|[System_Type](#system_type)|`nvarchar` Allowed: `C`, `M`, `T`|T=Task; C=Communication; M=Meeting|
|[Subject](#subject)|`nvarchar` |Task primary subject (required)|
|[Activity_Notes](#activity_notes)|`nvarchar` ||
|[Target_Party_Id](#target_party_id)|`uniqueidentifier` |External participant or target of the task|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |Who is responsible for executing the task. Initially this is the owner of the task|
|[Owner_Party_Id](#owner_party_id)|`uniqueidentifier` |The party that owns the task. Initially this is the party that has created the task|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority on the scale from 1 (least important) to 5 (very important)|
|[Private](#private)|`bit` |1 if the task is visible only to its owner; 0 if this is publicly visible task|
|[Activity_Start_Time](#activity_start_time)|`datetime` |Starting time of the task|
|[Deadline_Time](#deadline_time)|`datetime` |The deadline for the task. NULL if there is no deadline|
|[Activity_End_Time](#activity_end_time)|`datetime` |The time when the task was completed. NULL if the task is not yet completed|
|[Reminder_Time](#reminder_time)|`datetime` |When to snooze to the owner to remind him for the task|
|[Contact_Person_Id](#contact_person_id)|`uniqueidentifier` ||
|[Planned_Duration_Minutes](#planned_duration_minutes)|`int` |Total planned duration of the activity, regardless of the current execution status|
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the work is performed. NULL when the activity is not related to a project task.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The party which issued the document|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company that is issuing the document. NULL means that there is only one such company in the database and the reporting is always summarized|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[Document_Date](#document_date)|`date` ||
|[Reference_Date](#reference_date)|`datetime` |The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken|
|[Current_State](#current_state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` ||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly||
|[Adjustment_Number](#adjustment_number)|`int` Readonly|Consecutive number of the correction that this document is applying to the adjusted document.|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Creation_User](#creation_user)|`nvarchar` Readonly|The login name of the user, who created the document|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Void_User](#void_user)|`nvarchar` Readonly|The user who voided the document|
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly|Date/time when the document last has been adjusted by corrective document|
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly|The user who adjusted the document|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[Void_Reason](#void_reason)|`nvarchar` Readonly||
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Planning_Only](#planning_only)|`bit` Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)|
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` |The document that is the prime cause for creation of the current document|
|[Release_Time](#release_time)|`datetime` Readonly||
|[Complete_Time](#complete_time)|`datetime` Readonly||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.|
|[Reference_Document_No](#reference_document_no)|`nvarchar` |The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents|
|[Current_User_Status_Id](#current_user_status_id)|`uniqueidentifier` Readonly|The user status of this document if applicable for this document type. NULL means unknown or not yet set|
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` |The division of the company, issuing the document. NULL when the document is not issued by any specific division|
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` |The division of the company, receiving the document. NULL when the document is not received by any specific division|
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Activity_Time_Interval_Id](#activity_time_interval_id)|`uniqueidentifier` `PK`|The id of the time interval|
|[Activity_Id](#activity_id)|`uniqueidentifier` |The activity for which the time interval is recorded|
|[Party_Id](#party_id)|`uniqueidentifier` |The party for which the time interval is recorded|
|[Date](#date)|`date` |The date on which the work was performed|
|[Start_Time](#start_time)|`time` |The starting time of the time interval within 'Date'|
|[End_Time](#end_time)|`time` |The ending time of the time interval within 'Date'|
|[Notes](#notes)|`nvarchar` |Notes for the time interval|
|[Execution_Complete_Percent](#execution_complete_percent)|`decimal(0, 0)` |Percent of task completed|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|The state of the primary activity in the moment the time interval was created. NULL when the state is unknown.|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` |The user status of the primary activity in the moment the time interval was created. NULL when the user status is unknown.|

## Columns

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### System_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar|

### Activity_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Owner_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Private

| Property | Value |
| - | - |
|Type|bit|

### Activity_Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Deadline_Time

| Property | Value |
| - | - |
|Type|datetime|

### Activity_End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Reminder_Time

| Property | Value |
| - | - |
|Type|datetime|

### Contact_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Duration_Minutes

| Property | Value |
| - | - |
|Type|int|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### Current_State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Current_User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Activity_Time_Interval_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Date

| Property | Value |
| - | - |
|Type|date|

### Start_Time

| Property | Value |
| - | - |
|Type|time|

### End_Time

| Property | Value |
| - | - |
|Type|time|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Execution_Complete_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### State

| Property | Value |
| - | - |
|Type|smallint|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


