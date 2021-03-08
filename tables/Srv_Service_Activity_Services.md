# Table Srv_Service_Activity_Services

Contains the services, which were actually performed during the service activity (repair). Entity: Srv_Service_Activity_Services

# Aggregate Hierarchy

* [Srv_Service_Activities](Srv_Service_Activities.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Activity_Service_Id|`Guid`|`PK`, Readonly||
|Covered_By_Guarantee|`Boolean`||True when the performed service is covered by the guarantee. `Required` `Default(false)` |
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` |
|Notes|`String`||Short notes for the service. |
|Service_Name|`String`||Description of the conducted service. The description may vary (contain additional information) from the standart name of the service. `Required` `Filter(like)` |
