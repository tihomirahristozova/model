# Table Sys_Object_Changesets

A set of changes, performed in one request. Entity: Sys_Object_Changesets (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Object_Changeset_Id|`Guid`|`PK`, Readonly||
|Application_Name|`String`||The application which requested the change. null when it is unknown. `Filter(eq)` |
|Server_Version|`String`||The version of the application server at the time of the change. `Required` |
|Time_Utc|`DateTime`||Date and time (in Utc) when the changeset was processed by the server. `Required` `Default(NowUtc)` `Filter(eq;ge;le)` `ORD` |
