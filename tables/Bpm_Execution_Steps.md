# Table Bpm_Execution_Steps

Contains both historical and active steps in the execution of the business processes. Entity: Bpm_Execution_Steps

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Execution_Step_Id|`Guid`|`PK`, Readonly||
|Execution_State|`Int32`||Shows where the execution of the step has reached. 0=Ready; 10=Active; 20=Executing; 30=Completing; 40=Failing; 50=Terminating; 60=Completed; 70=Failed; 80=Terminated. `Required` `Default(0)` |
|Start_Time|`DateTime`||The date and time when the step execution started. `Required` `Default(Now)` |
