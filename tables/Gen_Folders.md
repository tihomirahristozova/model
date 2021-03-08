# Table Gen_Folders

Folders are the base for the file storage within the system. Each folder is a data object, with the primary idea of containing files. Entity: Gen_Folders (Introduced in version 21.1.1.8)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Folder_Id|`Guid`|`PK`, Readonly||
|Folder_Name|`String`||Name of the folder. Unique within its parent folder. `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this Folder. |
