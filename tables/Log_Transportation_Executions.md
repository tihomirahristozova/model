# Table Log_Transportation_Executions

Contains executions (loading, unloading or other operations) of the transportation orders. Entity: Log_Transportation_Executions (Introduced in version 18.2)

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Execution_Id|`Guid`|`PK`, Readonly||
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
|Execution_Date|`DateTime?`||Specifies the execution date, if it is the same for all lines. null means that the lines have different execution dates. |
|Execution_Time|`TimeSpan?`||Specifies the execution time, if it is the same for all lines. null means that the lines have different execution times. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
