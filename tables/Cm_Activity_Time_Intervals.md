# Table Cm_Activity_Time_Intervals

History of work efforts for executing activities (timesheet). Entity: Cm_Activity_Time_Intervals

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Activity_Time_Interval_Id|`Guid`|`PK`, Readonly||
|Date|`DateTime`||The date on which the work was performed. `Required` `Filter(eq;ge;le)` |
|End_Time|`TimeSpan`||The ending time of the time interval within 'Date'. `Required` `Filter(ge;le)` |
|Execution_Complete_Percent|`Decimal`||Percent of task completed. `Required` `Default(0)` `Filter(ge;le)` |
|Notes|`String`||Notes for the time interval. |
|Start_Time|`TimeSpan`||The starting time of the time interval within 'Date'. `Required` `Filter(ge;le)` |
|State|`DocumentState?`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|The state of the primary activity in the moment the time interval was created. null when the state is unknown. |
