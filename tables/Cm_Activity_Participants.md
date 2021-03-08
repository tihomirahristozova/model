# Table Cm_Activity_Participants

Contains the additional participants in the activities. These are the participating users, besides the user to which the activitiy is assigned. Entity: Cm_Activity_Participants

# Aggregate Hierarchy

* [Cm_Activities](Cm_Activities.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Activity_Participant_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this ActivityParticipant. |
|Work_Load_Percent|`Decimal`||The planned work load of the participant for this activity. `Required` `Default(1)` |
