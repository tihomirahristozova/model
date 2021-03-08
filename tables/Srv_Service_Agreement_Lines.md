# Table Srv_Service_Agreement_Lines

Service agreement lines represent the individual serviced objects that are covered by the service agreement. Entity: Srv_Service_Agreement_Lines

# Aggregate Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Service_Agreement_Object_Id|`Guid`|`PK`, Readonly||
|Line_End_Date_Time|`DateTime`||The ending date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)` |
|Line_No|`Int32`||Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` `Filter(eq)` |
|Line_Start_Date_Time|`DateTime`||The starting date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)` |
|Notes|`String`||Notes for this ServiceAgreementLine. |
|Quantity|`Decimal`||The quantity of the service object that is included in the agreement. `Required` `Default(1)` `Filter(ge;le)` |
