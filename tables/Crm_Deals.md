# Table Crm_Deals

Potential deals (Opportunities). Entity: Crm_Deals

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Deal_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Deal_Status|`DealStatus`|Allowed: `INP`, `SUC`, `UNS`|Current status of this deal. 'SUC' = Successful, 'UNS' = Unsuccessful, 'INP' = In progress. `Required` `Default("INP")` `Filter(multi eq)` |
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
|Revenue_End_Date|`DateTime`||Expected date on which the last revenue from this deal will occur. `Required` `Default(Today)` `Filter(ge;le)` |
|Revenue_Start_Date|`DateTime`||Expected date on which revenue from this deal will start. `Required` `Default(Today)` `Filter(ge;le)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Success_Probability|`Decimal`||Probability of success of that opportunity in percents (for example, 15 percent is stored as 0.15). `Required` `Default(0)` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
