# Table Bpm_Process_Lanes

The process lanes categorize elements in the process and contain logic for executor selection. Entity: Bpm_Process_Lanes

# Aggregate Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Lane_Id|`Guid`|`PK`, Readonly||
|Assign_By_User_Condition|`AssignByUserCondition`|Allowed: `N`, `R`, `L`|Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned. `Required` `Filter(eq;like)` |
|Is_System_Executed|`Boolean`||When set, specifies that the lane allows only system executed tasks and will never have human user as executor. `Required` `Default(false)` `Filter(eq)` |
|Locality|`Locality`|Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. `Required` `Filter(eq;like)` |
|Process_Lane_Name|`MultilanguageString`||Multilanguage lane name. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ProcessLane. |
|Restrict_To_Single_User|`Boolean`||Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user. `Required` `Default(false)` `Filter(eq)` |
|User_Condition_Filter_Xml|`DataAccessFilter`||User defined filter, used to select possible executors of tasks in the lane. `Filter(eq;like)` |
