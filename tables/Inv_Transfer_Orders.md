# Table Inv_Transfer_Orders

Orders for stock transfers between stores. Entity: Inv_Transfer_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transfer_Order_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Default_Due_Date_In|`DateTime`||The date, when the goods are expected to be received in the destination warehouse. `Required` `Default(Today)` `Filter(ge;le)` |
|Default_Due_Date_Out|`DateTime`||When the transfer is scheduled to issue the goods from the source warehouse. `Required` `Default(Today)` `Filter(ge;le)` |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this TransferOrder. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Status|`Status`|Allowed: `1`, `2`|Obsolete. Not used. (Status of the transfer document: 1-Open for editing; 2-Released). `Required` `Default(1)` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
