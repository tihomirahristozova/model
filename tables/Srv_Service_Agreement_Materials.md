# Table Srv_Service_Agreement_Materials

Contains the free materials, included in the service agreement. Entity: Srv_Service_Agreement_Materials

# Aggregate Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Agreement_Material_Id|`Guid`|`PK`, Readonly||
|End_Date|`DateTime?`||End date to which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities. |
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` |
|Start_Date|`DateTime?`||Start date from which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities. |
