# Table Crm_Offers

Offers (quotes) for sales of products. Can contain variants and choice groups. The user can select some approved lines and generate Sales Order. Entity: Crm_Offers

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Offer_Id|`Guid`|`PK`, Readonly||
|Accepted_On|`DateTime?`||The date on which the customer accepted the offer. null if the offer is not yet accepted or the date is unknown. |
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
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this Offer. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Payment_Due_Date|`DateTime?`||The last term for payment. |
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Required_Delivery_Date|`DateTime?`||When not null, specifies required delivery date for all offer lines. When the lines contain different delivery dates, this is null. |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Valid_Till|`DateTime?`||Last date when the offer is valid. null means the offer has no specific validity date. `Filter(ge;le)` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
