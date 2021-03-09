# Table Cm_Reminders

Reminders for activities. The reminders are alarms, which can be turned off. Each activity can have multiple reminders. Entity: Cm_Reminders

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Reminder_Id](#reminder_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` |The activity to which this reminder is attached|
|[Reminder_Time](#reminder_time)|`datetime` |The time when the alarm should snooze to the user|
|[Notes](#notes)|`nvarchar(2147483647)` |Notes that describe this specific reminder for the task|
|[Is_Dismissed](#is_dismissed)|`bit` |When 1 the reminder was dismissed by the user; the initial value is 0|
|[Is_Default](#is_default)|`bit` |1 when this is the defult reminder for a task. The default reminder is controlled through the task, while non-default reminders are manipulated through separate form|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Reminder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reminder_Time

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Dismissed

| Property | Value |
| - | - |
|Type|bit|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


