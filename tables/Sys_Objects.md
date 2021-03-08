# Table Sys_Objects

Extends data in other tables with attached files, custom properties, etc. Each row is an object, bound to exactly one row in the primary table. Each object can be bound to a row in a different primary table, specified in Entity_Type. Entity: Sys_Objects

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Object_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime?`||The exact server time (in UTC) when the object represented by this system object was created. null means that it is unknown. `Filter(ge;le)` `Introduced in version 19.1` |
|Entity_Item_Id|`Guid`||The Id of the primary row to which the object is bound. `Required` `Filter(multi eq)` |
|Entity_Type|`String`||The entity type of the row to which the object is bound. `Required` `Default(" ")` `Filter(eq)` `ORD` |
|Is_Deleted|`Boolean`||Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes. `Required` `Default(false)` `Filter(eq)` `Introduced in version 19.1` |
|Last_Update_Time_Utc|`DateTime?`||The exact server time (in UTC) of the last modification of the object represented by this system object. null means that it is unknown. `Filter(ge;le)` `Introduced in version 19.1` |
|Latest_Version|`Int32`||The latest saved version of the object. Starts from 1 and increments with 1 for each new version. `Required` `Default(1)` |
