# Table Bpm_Process_Instances

Contains the running instances of the processes. Entity: Bpm_Process_Instances

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Instance_Id|`Guid`|`PK`, Readonly||
|Creation_Time|`DateTime`|Readonly|The date and time, when the process instance was created. `Required` `Default(Now)` `Filter(eq)` `ReadOnly` |
|Finish_Time|`DateTime?`|Readonly|The date and time, when the process instance has finished its execution. null when the instance has not yet finished execution. `Filter(eq)` `ReadOnly` |
|Start_Time|`DateTime`|Readonly|The date and time, when the process instance was started. `Required` `Default(Now)` `Filter(eq)` `ReadOnly` |
|State|`State`|Allowed: `0`, `10`, `20`, `60`, Readonly|Instance state. 0=Created; 60=Completed. `Required` `Default(0)` `Filter(eq)` `ReadOnly` |
|Subject|`String`||The multilanguage subject (or title) of this process instance. `Required` `Filter(eq;like)` |
