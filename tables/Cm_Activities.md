# Table Cm_Activities

Generic activity. Provides task management functionality. Activity can be one of Task, Communication or Meeting. Entity: Cm_Activities

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Activity_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Deadline_Time|`DateTime?`||The deadline for the task. null if there is no deadline. `Filter(ge;le)` |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|End_Time|`DateTime?`||Currently planned ending time of the task. `Filter(ge;le)` |
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this Activity. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planned_Duration_Minutes|`Int32?`||Total planned duration of the activity, regardless of the current execution status. `Filter(ge;le)` |
|Planning_Only|`Boolean`|Readonly||
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority on the scale from 1 (least important) to 5 (very important). `Required` `Default(3)` |
|Private|`Boolean`||True if the task is visible only to its owner; false if this is publicly visible task. `Required` `Default(false)` |
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Reminder_Time|`DateTime?`||When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity. |
|Start_Time|`DateTime`||Currently planned starting time of the task. `Required` `Default(Now)` `Filter(ge;le)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Subject|`String`||Task primary subject (required). `Required` `Filter(eq;like)` |
|System_Type|`SystemType`|Allowed: `C`, `M`, `T`|T=Task; C=Communication; M=Meeting. `Required` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
