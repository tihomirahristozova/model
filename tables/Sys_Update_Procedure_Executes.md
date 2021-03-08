# Table Sys_Update_Procedure_Executes

Contains data about the execution of Upgrade Procedures. Contains status messages and ensures that each procedure is executed only once. Entity: Sys_Update_Procedure_Executes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Update_Procedure_Execute_Id|`Guid`|`PK`, Readonly||
|Execute_Time|`DateTime`||The time, when the update procedure was executed. `Required` `Default(Now)` |
|Result_Message|`String`||Error or success message. |
|Successful|`Boolean`||True when the execution was successfull. `Required` `Default(true)` |
|Update_Procedure|`String`||The system name of the executed update procedure. `Required` |
