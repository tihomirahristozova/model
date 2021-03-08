# Table Gen_Work_Schedule_Working_Time

Contains the different working time periods within the work schedule. Entity: Gen_Work_Schedule_Working_Time

# Aggregate Hierarchy

* [Gen_Work_Schedules](Gen_Work_Schedules.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Day_No|`Int32`||Consequtive day in the work schedule recurrence, starting at 1. `Required` |
|End_Time|`TimeSpan`||End of working time period. `Required` |
|Start_Time|`TimeSpan`||Start of working time period on the day, specified by Day_No. `Required` |
