# Table Bpm_Process_Node_Timer_Events

Timer event definition. Currently - not used. Entity: Bpm_Process_Node_Timer_Events

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Node_Timer_Event_Id|`Guid`|`PK`, Readonly||
|Process_Node_Event_Id|`Guid`||The process node event, which this timer defines. `Required` `Filter(multi eq)` |
|Time_Cycle|`String`||Non-null when the timer is recurring. The value conforms to the ISO-8601 format for recurring time intervals. Mutually exclusive with the other Time fields. |
|Time_Date|`DateTime?`||Non-null when the timer is for specific single date and time. Mutually exclusive with the other Time fields. |
|Time_Duration|`String`||Non-null when the timer event is for time duration. The value conforms to the ISO-8601 format for time interval representations. Mutually exclusive with the other Time fields. |
