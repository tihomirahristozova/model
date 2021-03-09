# Table Bpm_Process_Node_Timer_Events

Timer event definition. Currently - not used. Entity: Bpm_Process_Node_Timer_Events

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Node_Timer_Event_Id](#process_node_timer_event_id)|`uniqueidentifier` `PK`||
|[Process_Node_Event_Id](#process_node_event_id)|`uniqueidentifier` |The process node event, which this timer defines.|
|[Time_Date](#time_date)|`datetime` |Non-null when the timer is for specific single date and time. Mutually exclusive with the other Time fields.|
|[Time_Cycle](#time_cycle)|`nvarchar(128)` |Non-null when the timer is recurring. The value conforms to the ISO-8601 format for recurring time intervals. Mutually exclusive with the other Time fields.|
|[Time_Duration](#time_duration)|`nvarchar(128)` |Non-null when the timer event is for time duration. The value conforms to the ISO-8601 format for time interval representations. Mutually exclusive with the other Time fields.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Node_Timer_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Node_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time_Date

| Property | Value |
| - | - |
|Type|datetime|

### Time_Cycle

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Time_Duration

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


