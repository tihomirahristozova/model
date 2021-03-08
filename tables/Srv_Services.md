# Table Srv_Services

Contains the services, which can be performed. Entity: Srv_Services

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Id|`Guid`|`PK`, Readonly||
|Service_Code|`String`||Unique code of the service. `Required` `Filter(eq;like)` |
|Is_Active|`Boolean`||Indicates wheather this service is currently used. `Required` `Default(true)` `Filter(eq)` |
|Service_Name|`String`||The name of the service. `Required` `Filter(eq;like)` |
