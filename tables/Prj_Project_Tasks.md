# Table Prj_Project_Tasks

Represents one task of a project. Entity: Prj_Project_Tasks

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Task_Id|`Guid`|`PK`, Readonly||
|Finish_Date_Time|`DateTime`||The date and time when the task is planned to finish. `Required` `Default(Now)` `Filter(eq;ge;le)` |
|Notes|`String`||Notes for this ProjectTask. |
|Planned_Duration_Hours|`Decimal`||Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time. `Required` `Default(0)` |
|Project_Task_No|`Int32`||Consecutive task number, unique within the project. `Required` |
|Start_Date_Time|`DateTime`||The date and time when the task is planned to start. `Required` `Default(Now)` `Filter(eq;ge;le)` |
|Task_Name|`String`||The short name of the task. It is best practice to contain the target of the task. `Required` `Filter(multi eq;like)` |
