# Table Gen_Document_Versions

History of each saved version of each document. Entity: Gen_Document_Versions

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Version_Id|`Guid`|`PK`, Readonly||
|Document_Data|`Byte[]`|`BLOB`, Readonly|Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed). `ReadOnly` |
|Document_Data_Format|`String`|Readonly|The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data. `Required` `Default("U")` `ReadOnly` |
|Document_Data_XML|`String`|Readonly|The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed). `ReadOnly` |
|State|`State`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The state of the document by the time it was saved. `Required` `Default(0)` `Filter(multi eq)` `ReadOnly` |
|Update_Time|`DateTime`|Readonly|The date and time when this version was saved. `Required` `Default(Now)` `Filter(ge;le)` `ORD` `ReadOnly` |
|Update_User|`String`|Readonly|The login name of the user that saved this version. `Required` `Filter(eq;like)` `ReadOnly` |
|Version|`Int32`|Readonly|The version number that is stored in this row. `Required` `Filter(eq;ge;le)` `ReadOnly` |
