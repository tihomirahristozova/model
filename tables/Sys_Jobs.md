# Table Sys_Jobs

The jobs, which are configured in the system. Entity: Sys_Jobs (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Job_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Specifies whether the job is active and ready for running. `Required` `Default(true)` `Filter(eq)` |
|Job_Type|`JobType`|Allowed: `DOC`, `POS`, `DNT`, `DPI`|The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. `Required` `Filter(multi eq)` |
|Job_Name|`String`||The name of the job. `Required` `Filter(eq;like)` `ORD` |
|Notes|`String`||Notes for this Job. |
|Run_On_Idle|`Boolean`||Specifies whether to automatically run the job when the server is idle. `Required` `Default(true)` `Filter(eq)` |
