# Table Scm_Receiving_Orders

Contains the received quantities from a supplier. Entity: Scm_Receiving_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Receiving_Order_Id|`Guid`|`PK`, Readonly||
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
|Invoice_Document_No|`String`||Contains the purchase invoice number when it is known in advance, null otherwise. `Filter(eq)` |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this ReceivingOrder. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Payment_Due_Date|`DateTime?`||Due date for the payment. When null, the payment due date is the documents date. `Filter(ge;le)` |
|Planned_Delivery_Date|`DateTime?`||When not null, specifies the planned delivery date for all lines. `Filter(ge;le)` |
|Planned_Release_Date|`DateTime?`||The date, when the document is planned to be realeased. `Filter(ge;le)` |
|Planning_Only|`Boolean`|Readonly||
|Purchase_Lot_Description|`String`||Description of the purchase lot for the whole document. It is set for the lots created by this receiving order. |
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
