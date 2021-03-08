# Table Gen_Work_Schedules

Represents the different working schedules, used by the employees and resources. Entity: Gen_Work_Schedules

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Work_Schedule_Name|`String`||The name of this WorkSchedule. `Required` `Filter(like)` |
|Number_Of_Days|`Int16?`||Number of days in a recurring period. Valid only when Recurrence_Type=D. |
|Recurrence_Type|`RecurrenceType`|Allowed: `D`, `M`, `W`|D=recurring each X days; W=recurring each week; M=recurring each month. `Required` `Filter(multi eq)` |
