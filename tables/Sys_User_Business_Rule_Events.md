# Table Sys_User_Business_Rule_Events

Represents event registration of a business rule. Entity: Sys_User_Business_Rule_Events

# Aggregate Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Business_Rule_Event_Id|`Guid`|`PK`, Readonly||
|Event_Parameter|`String`||Registration parameter. The meaning is determined by the event. Usually - attribute name, document state, etc. |
|Event_Type|`EventType`|Allowed: `AGGREGATECLIENTCOMMIT`, `ATTRIBUTECHANGED`, `ATTRIBUTECHANGING`, `CLIENTCOMMIT`, `COMMIT`, `STATECHANGED`, `STATECHANGING`, `VOIDING`|The event for which to register the business rule. `Required` |
|Execution_Priority|`RuleExecutionPriority`|Allowed: `30`, `50`, `70`, `150`, `200`|Execution priority. Lower values indicate earlier priorities. Possible values - 30-Early, 50-Normal, 70-Late. `Required` `Default(50)` |
|Layer|`Layer`|Allowed: `FTE`, `BKE`|Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd. `Required` `Default("BKE")` |
