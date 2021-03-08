# Table Srv_Service_Types

Service levels. Entity: Srv_Service_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Type_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this ServiceType. |
|Is_Active|`Boolean`||True when the service type is currently active and selectable in new documents. `Required` `Default(true)` `Filter(eq)` |
|Is_Default|`Boolean`||True when this is the default service type for the service object type. false otherwise. `Required` `Default(false)` `Filter(eq)` |
|Service_Type_Name|`String`||The name of this ServiceType. `Required` `Filter(like)` |
