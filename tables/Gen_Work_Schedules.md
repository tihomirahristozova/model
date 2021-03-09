# Table Gen_Work_Schedules

Represents the different working schedules, used by the employees and resources. Entity: Gen_Work_Schedules

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|work schedule id|
|[Work_Schedule_Name](#work_schedule_name)|`nvarchar(64)` ||
|[Recurrence_Type](#recurrence_type)|`nvarchar(1)` Allowed: `D`, `M`, `W`|D=recurring each X days; W=recurring each week; M=recurring each month|
|[Number_Of_Days](#number_of_days)|`smallint` |Number of days in a recurring period. Valid only when Recurrence_Type=D|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Schedule_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Recurrence_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Number_Of_Days

| Property | Value |
| - | - |
|Type|smallint|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


