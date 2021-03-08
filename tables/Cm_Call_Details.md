# Table Cm_Call_Details

Contains call detail records. Calls are phone calls, video calls and SMS messages. Entity: Cm_Call_Details

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Call_Detail_Record_Id|`Guid`|`PK`, Readonly||
|Called_Party_Number|`String`||The voice number of the party, which received the call. `Required` `Filter(eq;like)` |
|Calling_Party_Number|`String`||The voice number of the originating party of the call. `Required` `Filter(eq;like)` |
|Call_Type|`CallType`|Allowed: `P`, `V`, `M`|P=Phone; V=Video; M=Message/SMS. `Required` `Default("P")` `Filter(eq)` |
|Call_Unique_Id|`String`||The unique id of the call, as reported by the telephone central. null when the central did not report unique Id. Used for integration purposes. |
|Duration_Seconds|`Int32`||The duration of the call (in seconds). `Required` `Default(0)` `Filter(ge;le)` |
|Start_Time|`DateTime`||The starting date and time of the call. `Required` `Filter(ge;le)` |
