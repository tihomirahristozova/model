# Table Bpm_Process_Connections

Contains the connections between process elements. Part of the process model. Entity: Bpm_Process_Connections

# Aggregate Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Connection_Id|`Guid`|`PK`, Readonly||
|Process_Connection_Code|`String`||Connection code, unique within the process. Used as ID for XML serialization purposes. `Required` `Default(New Guid)` `Filter(eq;like)` |
|Condition_Filter_Xml|`DataAccessFilter`||When not null, specifies that the flow will be followed only if the condition is matched by the current values in the process instance. `Filter(eq;like)` |
|Is_Default|`Boolean`||Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow. `Required` `Default(false)` `Filter(eq)` |
|Process_Connection_Name|`MultilanguageString`||Multilanguage connection name. `Required` `Filter(eq;like)` |
