# Table Gen_Link_Types

Obsolete. Not used. Entity: Gen_Link_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Code|`Guid`|`PK`, Readonly||
|From_Doc_Type_Id|`Guid?`||From which type of documents the link originates. null means that it might originate from any document type. `Filter(multi eq)` |
|Link_Type_Name|`String`||Obsolete. Not used. `Required` |
|To_Doc_Type_Id|`Guid?`||To what type of documents the link points. null means that it might point to any document type. `Filter(multi eq)` |
