# Table Cm_Contact_Mechanism_Purposes

Contains user-defined purposes for processing contact mechanisms. Used for personal data management. Entity: Cm_Contact_Mechanism_Purposes (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Contact_Mechanism_Purpose_Id|`Guid`|`PK`, Readonly||
|Code|`String`||The unique code of the ContactMechanismPurpos. `Required` `Filter(eq;like)` `ORD` |
|Contact_Mechanism_Type|`ContactMechanismType?`|Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|When specified, allows the purpose to be specified only for contact mechanisms of the specified type. `Filter(multi eq)` |
|Description|`String`||The description of this ContactMechanismPurpos. `Filter(like)` |
|Name|`MultilanguageString`||Name of the contact mechanism purpose (Multilanguage). `Required` `Filter(like)` |
