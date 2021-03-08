# Table VAT_Entries

Contains the entries in the VAT sales and purchase ledgers. Entity: VAT_Entries

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Entry_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Apply_Date|`DateTime`||Specifies the date on which the entry should be applied in the reporting. Usually equal to the document date with exception for documents that are late to be applied in the correct period. `Required` `Filter(ge;le)` |
|Cash_Reporting_Mode|`Boolean`||When true, specifies, that the special cash reporting mode should be used for VAT reporting. When false, the normal (classic) VAT reporting is used. `Required` `Default(false)` |
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Entry_Type|`EntryType`|Allowed: `P`, `S`|Type of the VAT entry. S=Sales, P=Purchases. `Required` `Filter(eq)` `ORD` |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Referenced_Document_No|`String`||Number of the document that represents the operation that caused this entry. `Required` `Filter(eq)` |
|Reference_Document_No|`String`|||
|Registration_Number|`String`||Identification code (IC) for the party specified by Party_Id. |
|Registration_VAT_Number|`String`||VAT number by registration (or national number) for the party specified by Party_Id. `Required` `Filter(eq)` |
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
