# Table Nat_BG_VAT_Declarations

National data: Contains the VAT declarations, issued by the enterprise company, according to the Bulgarian legislation. Entity: Nat_BG_VAT_Declarations

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|VAT_Declaration_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Coefficient_VATL_Article_73|`Decimal`||Field 01 - 33 from the declaration. Must be between 0.00 and 1.00. `Required` `Default(0)` |
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
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|VAT_Declaration_Representing_Person_Position|`String`||Position of the representing person for the purposes of submitting of VAT declarations. |
|VAT_Period_End|`DateTime`||End date of the period fot which the VAT declaration is made. `Required` `Filter(ge;le)` |
|VAT_Period_Start|`DateTime`||Start date of the period fot which the VAT declaration is made. `Required` `Filter(ge;le)` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
