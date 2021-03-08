# Table Srv_Service_Order_Lines

Contains the details and problem symptoms for each object, which requires servicing. Entity: Srv_Service_Order_Lines

# Aggregate Hierarchy

* [Srv_Service_Orders](Srv_Service_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Order_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` `Filter(eq)` |
|Symptom_Description|`String`||Description or synopsis of the symptoms of the failed object. `Filter(like)` |
