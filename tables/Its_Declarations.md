# Table Its_Declarations

Contains the headers of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declarations

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Intrastat_Declaration_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Declaration_Function|`DeclarationFunction`|Allowed: `R`, `C`|Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective. `Required` `Default("R")` `Filter(eq)` |
|Declare_Statistical_Values|`Boolean`||Does the declaration contain statistical values? true=Yes; false=No. `Required` `Default(false)` `Filter(multi eq)` |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Goods_Flow_Direction|`GoodsFlowDirection`|Allowed: `A`, `D`|The flow direction of the goods. A=Arrival, D=Dispatch. `Required` `Filter(eq)` |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Postal_Code|`String`||This field contains the postal code part of the submitter’s address. `Required` |
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Reference_Month|`ReferenceMonth`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`|Month, for which the declaration is prepared. `Required` `Filter(eq)` |
|Reference_Year|`Int16`||Year, for which the declaration is prepared. `Required` `Filter(eq)` |
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
