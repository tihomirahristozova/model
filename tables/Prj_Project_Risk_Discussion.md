# Table Prj_Project_Risk_Discussion

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

# Aggregate Hierarchy

* [Prj_Project_Risks](Prj_Project_Risks.md)
* [Prj_Projects](Prj_Projects.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Risk_Message_Id|`Guid`|`PK`, Readonly||
|Contribution_Time|`DateTime`|Readonly|The time, when the message was contributed. `Required` `Default(Now)` `Filter(eq)` `ReadOnly` |
|Last_Edit_Time|`DateTime?`|Readonly|Contains the last edit time of the message. null if the message was never edited. `Filter(eq)` `ReadOnly` |
|Message|`String`||The contents of the message. `Required` |
