# Table Wms_Warehouse_Requisitions

Contains request for warehouse operation created from another module. Entity: Wms_Warehouse_Requisitions (Introduced in version 20.1)

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Requisition_Id|`Guid`|`PK`, Readonly||
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
|Expected_Date|`DateTime`||Date, when the requisition is expected to be fulfilled. `Required` `Default(Today)` `Filter(multi eq;ge;le)` |
|Expected_Time|`TimeSpan?`||Time, when the requisition is expected to be executed. null when the time is unknown. `Filter(eq;ge;le)` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Requisition_Type|`RequisitionType`|Allowed: `I`, `O`|The type of the requisition. I=Inbound; O=Outbound. `Required` `Filter(multi eq)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
