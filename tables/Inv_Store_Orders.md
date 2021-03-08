# Table Inv_Store_Orders

Orders for store transactions. After an order is executed, store transaction is created. Entity: Inv_Store_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Store_Order_Id|`Guid`|`PK`, Readonly||
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
|Driver_Name|`String`||The name of the driver, who will deliver the stocks. |
|Due_Date|`DateTime`||The final date, when the store transaction should occur. `Required` `Default(Today)` `Filter(ge;le)` `ORD` |
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Movement_Type|`MovementType`|Allowed: `I`, `R`|Store order movement type. R=RECEIPT, I=ISSUE. `Required` `Default("R")` `Filter(multi eq)` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planned_Completion_Date|`DateTime?`||Date, when the quantities are expected to be completely issued/received. `Filter(ge;le)` |
|Planned_Release_Date|`DateTime?`||Date, when the respective store transaction document is scheduled to be released to the supplier or manufacturing. This is respected by all PAB (projected available balance) and ATP (available to promise) calculations as the date on which the store transaction is scheduled to occur. `Filter(ge;le)` |
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Status|`String`||P=Planned; F=Firm planned; R=Released; C=Completed. `Required` `Default("P")` |
|Temp_Transport_Company_Name|`String`||Obsolete. Not used. |
|Vehicle_Reg_Number|`String`||Obsolete. Not used. |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
