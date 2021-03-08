# Table Gen_Document_Comments

Contains user comments for documents. Entity: Gen_Document_Comments

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Comment_Id|`Guid`|`PK`, Readonly||
|Comment|`String`||The user comment. `Required` |
|Comment_Timestamp|`DateTime`||The exact timestamp of the comment. `Required` `Default(Now)` |
