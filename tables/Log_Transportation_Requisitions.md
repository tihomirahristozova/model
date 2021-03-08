# Table Log_Transportation_Requisitions

Client requisition for transportation. Entity: Log_Transportation_Requisitions

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Requisition_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Requested_Arrival_Date|`DateTime`||Requested arrival date. null when no specific date is requested. `Required` `Filter(ge;le)` |
|Requested_Arrival_Time|`TimeSpan?`||Requested arrival time. null when no specific time is requested. `Filter(ge;le)` |
|Requested_Departure_Date|`DateTime`||Requested date of departure. null when no specific date is requested. `Required` `Filter(ge;le)` |
|Requested_Departure_Time|`TimeSpan?`||Requested time of departure. null when no specific time is requested. `Filter(ge;le)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
