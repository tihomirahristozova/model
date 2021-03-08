# Table Srv_Service_Agreement_Services

Contains the free services, included in the service agreement. Entity: Srv_Service_Agreement_Services

# Aggregate Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Agreement_Service_Id|`Guid`|`PK`, Readonly||
|End_Date|`DateTime?`||End date to which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities. |
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` |
|Start_Date|`DateTime?`||Start date from which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities. |
