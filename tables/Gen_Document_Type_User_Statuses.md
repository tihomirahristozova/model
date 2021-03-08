# Table Gen_Document_Type_User_Statuses

User-defined document statuses. Entity: Gen_Document_Type_User_Statuses

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Status_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||Is the user status active for applying to documents. `Required` `Default(true)` `Filter(eq)` |
|Display_Order|`Int32`||Consecutive display order of the status, with regard to other statuses within the same document type. `Required` `Filter(ge;le)` |
|Instructions|`String`||Instructions what should be done when this user status is active (Rich Text). |
|Is_Exit_Status|`Boolean`||True when the status allows going to the next system status, false otherwise. For example for system status Firm Planned, only user status Approved might allow going to Released. `Required` `Default(true)` `Filter(eq)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|The system state to which this user status is bound. `Required` `Filter(eq)` |
|User_Status_Name|`String`||Multi-language name of the user status. `Required` `Filter(eq;like)` |
