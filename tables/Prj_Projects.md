# Table Prj_Projects

Contains the planned, running and completed projects of the enterprises. Entity: Prj_Projects

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Id|`Guid`|`PK`, Readonly||
|Project_Code|`String`||Short code for identification of projects. `Required` `Filter(eq;like)` `ORD` |
|Finish_Date|`DateTime?`||The drop dead date of the project, e.g. the date when the project should be finished. null means that the finish date is unknown. `Filter(eq)` |
|Project_Name|`String`||The name of this Project. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this Project. |
|Project_Status|`ProjectStatus`|Allowed: `0`, `10`, `20`, `30`, `40`, `45`, `50`, `55`|Current project status. 0=New/Structuring, 10=Budgeting, 20=Panning, 30=Started, 40=Resolved(Completed), 45=Resolved(Cancelled), 50=Closed(Completed), 55=Closed(Cancelled). `Required` `Default(0)` `Filter(multi eq)` |
|Start_Date|`DateTime?`||Expected date, when the execution of the tasks will start. null means that the start date is still unknown. `Filter(eq)` |
