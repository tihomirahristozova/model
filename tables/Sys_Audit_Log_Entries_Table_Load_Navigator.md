# Query Sys_Audit_Log_Entries_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Audit_Log_Entry_Id](#audit_log_entry_id)|`uniqueidentifier` `PK`||
|[Event_Time_Utc](#event_time_utc)|`datetime` |The exact date and time (in Utc) when the event occurred.|
|[Event_Class](#event_class)|`nvarchar` Allowed: `E`, `A`, `S`|The event primary classification, which shows the source of the event. E=Entity methods; A=Auth events; S=Server events.|
|[Event_Type](#event_type)|`nvarchar` Allowed: `EID`, `ELD`, `ECR`, `EUP`, `EDE`, `EMT`, `ETH`, `AIN`, `AOU`, `AUP`, `AFL`, `APW`, `ATH`, `STH`|Detailed action type. EID=Read one record by Id; ELD=Load many records; EUP=Update data; EDE=Delete record; EMT=Call method; ETH=Other entity event; AIN=Login; AOU=Log out; AUP=Sign Up; AFL=Login failed; APW=Change password; ATH=Other auth event; STH=Other server event.|
|[Event_Name](#event_name)|`nvarchar` |Specific event or method name. Contents depend on the Event Type. Null when N/A.|
|[Entity_Name](#entity_name)|`nvarchar` |The entity, which is being referenced by the event. Null when unknown or N/A.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The Id of the record, which is referenced by the event. Null when unknown or N/A.|
|[User_Id](#user_id)|`uniqueidentifier` |The user account under which the event has occurred. Null only for events which are not user-specific.|
|[Details](#details)|`nvarchar` |Detailed contents of the event. Contents depend on the Event Type and Event Name.|
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The personal data process, which was used to process the data, referenced by the event. Null when unknown or N/A.|
|[Application_Name](#application_name)|`nvarchar` |The client application that triggered the event. Null when unknown or N/A.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Audit_Log_Entry_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Event_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Event_Class

| Property | Value |
| - | - |
|Type|nvarchar|

### Event_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Event_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Details

| Property | Value |
| - | - |
|Type|nvarchar|

### Personal_Data_Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


