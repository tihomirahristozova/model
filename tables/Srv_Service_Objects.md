# Table Srv_Service_Objects

Contains the serviceable objects. The service objects can be covered by service agreements, serviced in service activities, etc. Entity: Srv_Service_Objects

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Object_Id|`Guid`|`PK`, Readonly||
|Service_Object_Name|`String`||The name of this ServiceObject. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ServiceObject. |
|Serial_Number|`String`||The serial number of the item, that is being serviced. `Filter(like)` |
