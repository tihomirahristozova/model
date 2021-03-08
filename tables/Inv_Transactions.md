# Table Inv_Transactions

Executed store-receipts(in) and store-issues(out). Store-issues are recorded with minus quantity. Entity: Inv_Transactions

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transaction_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Cost_Source|`CostSource`|Allowed: `S`, `D`, Readonly|Determines whether the cost in the transaction is taken from the store current availability (usually this is the case for issue transactions) or the cost must be specified in the transaction itself (usually for receipt transactions). S = Store, D = Document. `Required` `ReadOnly` |
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Scrap|`Boolean`||False=Non-scrap; true=Scrap operation. Only store issue operations can be scrap. `Required` `Default(false)` `Filter(eq)` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|IsValid|`Boolean`|Readonly|Managed by the system and used only for integrity purposes. Do not use. `Required` `Default(false)` `ReadOnly` |
|Movement_Type|`MovementType`|Allowed: `I`, `R`|Transaction movement type. R=RECEIPT, I=ISSUE. `Required` `Default("R")` `Filter(multi eq)` |
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
