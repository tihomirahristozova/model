# Table Inv_Cost_Corrections

Cost corrections provide a way to correct the cost of stock transactions after they are issued. Entity: Inv_Cost_Corrections

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Correction_Id|`Guid`|`PK`, Readonly||
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
|From_Date|`DateTime`||The date from which to start looking for transactions, needing cost correction. It is used only when the source transaction is null. `Required` |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Thru_Date|`DateTime`||The date at which to stop looking for transactions, needing cost correction. It is used only when the source transaction is null. `Required` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
