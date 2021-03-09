# Table Cm_Activity_Time_Intervals

History of work efforts for executing activities (timesheet). Entity: Cm_Activity_Time_Intervals

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Activity_Time_Interval_Id](#activity_time_interval_id)|`uniqueidentifier` `PK`|The id of the time interval|
|[Activity_Id](#activity_id)|`uniqueidentifier` |The activity for which the time interval is recorded|
|[Party_Id](#party_id)|`uniqueidentifier` |The party for which the time interval is recorded|
|[Date](#date)|`date` |The date on which the work was performed|
|[Start_Time](#start_time)|`time` |The starting time of the time interval within 'Date'|
|[End_Time](#end_time)|`time` |The ending time of the time interval within 'Date'|
|[Notes](#notes)|`nvarchar(254)` |Notes for the time interval|
|[Execution_Complete_Percent](#execution_complete_percent)|`decimal(3, 2)` |Percent of task completed|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|The state of the primary activity in the moment the time interval was created. NULL when the state is unknown.|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` |The user status of the primary activity in the moment the time interval was created. NULL when the user status is unknown.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

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
|Type|nvarchar(254)|

### Execution_Complete_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### State

| Property | Value |
| - | - |
|Type|smallint|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


