# Table Cmm_Social_Reactions

Reaction of a user to any social comment to an object of the system. Entity: Cmm_Social_Reactions (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Social_Reaction_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`||The exact server time (in UTC), when the reaction was created. `Required` `Default(NowUtc)` |
|Reaction_Type|`ReactionType`|Allowed: `LIK`, `LOV`, `HAH`, `WOW`, `SAD`, `ANG`|The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry. `Required` `Filter(multi eq)` |
