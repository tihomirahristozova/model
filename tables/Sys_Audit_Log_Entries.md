# Table Sys_Audit_Log_Entries

Each record represents the occurrence of one logged event. Entity: Sys_Audit_Log_Entries (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Audit_Log_Entry_Id|`Guid`|`PK`, Readonly||
|Application_Name|`String`||The client application that triggered the event. Null when unknown or N/A. `Filter(eq;like)` |
|Details|`String`||Detailed contents of the event. Contents depend on the Event Type and Event Name. |
|Entity_Item_Id|`Guid?`||The Id of the record, which is referenced by the event. Null when unknown or N/A. `Filter(multi eq)` |
|Entity_Name|`String`||The entity, which is being referenced by the event. Null when unknown or N/A. `Filter(eq;like)` |
|Event_Class|`EventClass`|Allowed: `E`, `A`, `S`|The event primary classification, which shows the source of the event. E=Entity methods; A=Auth events; S=Server events. `Required` `Filter(multi eq)` |
|Event_Name|`String`||Specific event or method name. Contents depend on the Event Type. Null when N/A. `Filter(eq;like)` |
|Event_Time_Utc|`DateTime`||The exact date and time (in Utc) when the event occurred. `Required` `Default(Now)` `Filter(ge;le)` `ORD` |
|Event_Type|`EventType`|Allowed: `EID`, `ELD`, `ECR`, `EUP`, `EDE`, `EMT`, `ETH`, `AIN`, `AOU`, `AUP`, `AFL`, `APW`, `ATH`, `STH`|Detailed action type. EID=Read one record by Id; ELD=Load many records; EUP=Update data; EDE=Delete record; EMT=Call method; ETH=Other entity event; AIN=Login; AOU=Log out; AUP=Sign Up; AFL=Login failed; APW=Change password; ATH=Other auth event; STH=Other server event. `Required` `Filter(multi eq)` |
