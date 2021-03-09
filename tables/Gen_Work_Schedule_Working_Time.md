# Table Gen_Work_Schedule_Working_Time

Contains the different working time periods within the work schedule. Entity: Gen_Work_Schedule_Working_Time

## Owner Tables Hierarchy

* [Gen_Work_Schedules](Gen_Work_Schedules.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Schedule_Id](#work_schedule_id)|`uniqueidentifier` ||
|[Day_No](#day_no)|`int` |Consequtive day in the work schedule recurrence, starting at 1|
|[Start_Time](#start_time)|`time` |Start of working time period on the day, specified by Day_No|
|[End_Time](#end_time)|`time` |End of working time period|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Day_No

| Property | Value |
| - | - |
|Type|int|

### Start_Time

| Property | Value |
| - | - |
|Type|time|

### End_Time

| Property | Value |
| - | - |
|Type|time|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


