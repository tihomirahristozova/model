# Table Srv_Service_Activity_Materials

Contains the materials, which were actually used during the service activity (repair). Entity: Srv_Service_Activity_Materials

# Aggregate Hierarchy

* [Srv_Service_Activities](Srv_Service_Activities.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Activity_Material_Id|`Guid`|`PK`, Readonly||
|Covered_By_Guarantee|`Boolean`||True when the used material is covered by the guarantee. `Required` `Default(false)` |
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` |
