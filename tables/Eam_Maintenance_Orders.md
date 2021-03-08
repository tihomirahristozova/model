# Table Eam_Maintenance_Orders

Orders for maintenance. It is performed by a single service center, but can contain many different types of maintenance for many assets. The document is Activity and as such is scheduled and visible in the main calendar. Entity: Eam_Maintenance_Orders (Introduced in version 19.1)

# Inheritance

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Maintenance_Order_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Deadline_Time|`DateTime?`|||
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|End_Time|`DateTime?`|||
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly||
|Is_Single_Execution|`Boolean`|Readonly||
|Notes|`String`|||
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planned_Duration_Minutes|`Int32?`|||
|Planning_Only|`Boolean`|Readonly||
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`||
|Private|`Boolean`|||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Reminder_Time|`DateTime?`|||
|Start_Time|`DateTime`|||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Subject|`String`|||
|System_Type|`SystemType`|Allowed: `C`, `M`, `T`||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
