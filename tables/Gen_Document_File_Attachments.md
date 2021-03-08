# Table Gen_Document_File_Attachments

Contains files, attached to the documents. Entity: Gen_Document_File_Attachments

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_File_Id|`Guid`|`PK`, Readonly||
|Embedded_File_Contents|`Byte[]`|`BLOB`|The contents of the embedded file. null when the file is linked. |
|File_Name|`String`||The display name of the file. Initially set to the file name (without path) of the linked or the embedded file. `Required` |
|Is_Linked|`Boolean`||True when the document is linked (ony file name is kept). false when the document is embedded. `Required` `Default(false)` `Filter(eq)` |
|Linked_File_Path|`String`||Path to the linked file. null when the file is embedded. |
|Notes|`String`||Notes for this DocumentFileAttachment. |
