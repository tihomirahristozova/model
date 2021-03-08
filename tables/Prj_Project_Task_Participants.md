# Table Prj_Project_Task_Participants

Contains the participants in the project tasks. Entity: Prj_Project_Task_Participants

# Aggregate Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Task_Participant_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this ProjectTaskParticipant. |
|Notify_On_Status_Change|`Boolean`||Specifies whether the participant should be notified on task status changes. `Required` `Default(true)` |
|Work_Load_Percent|`Decimal`||The planned work load (in percents) of the participant for this task. `Required` `Default(1)` `Filter(eq)` |
