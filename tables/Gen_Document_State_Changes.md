# Table Gen_Document_State_Changes

History of document state changes. Entity: Gen_Document_State_Changes

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_State_Change_Id|`Guid`|`PK`, Readonly||
|New_State|`NewState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|The new state after the change. `Required` `Filter(eq)` |
|System_Initiated|`Boolean`|Readonly|Specifies whether the state change was caused by system process or from user action. `Required` `Default(false)` `ReadOnly` |
|Update_Time|`DateTime`||The time when the change took effect. `Required` `Filter(ge;le)` `ORD` |
|Update_User|`String`||The login name of the user, who made the status change. `Required` `Filter(eq)` |
|Void|`Boolean`||True if the document is voided with this change. `Required` `Default(false)` `Filter(eq)` `Introduced in version 19.1` |
