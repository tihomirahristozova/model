# Table Gen_Scheduled_Document_Events

Contains postponed events, which will be executed later. Usually these are large number of recalculation events, resulting from other events. For example, releasing a cost correction, publishes postponed events for all affected documents. Entity: Gen_Scheduled_Document_Events

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Scheduled_Document_Event_Id|`Guid`|`PK`, Readonly||
|Cancelled|`Boolean`||When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed. `Required` `Default(false)` `Filter(eq)` |
|Creation_Time|`DateTime`|Readonly|Date and time when the ScheduledDocumentEvent was created. `Required` `Default(Now)` `ReadOnly` |
|Document_Event|`String`|Readonly|The type of the document event that is scheduled to be processed. `Required` `ReadOnly` |
|Last_Process_Status|`String`|Readonly|Status/information of the last attemp to process the event. Usually shows the cause in case of failure. `ReadOnly` |
|Last_Process_Time|`DateTime?`|Readonly|The time of the last attempt to process the event. `ReadOnly` |
|Processed|`Boolean`|Readonly|Indicates wheather the event is already processed or not. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|State|`State`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The state of the document for which the event will be processed. `Required` `ReadOnly` |
