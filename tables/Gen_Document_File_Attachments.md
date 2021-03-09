# Table Gen_Document_File_Attachments

Contains files, attached to the documents. Entity: Gen_Document_File_Attachments

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[File_Name](#file_name)|`nvarchar(128)` |The display name of the file. Initially set to the file name (without path) of the linked or the embedded file|
|[Is_Linked](#is_linked)|`bit` |1 when the document is linked (ony file name is kept). 0 when the document is embedded|
|[Linked_File_Path](#linked_file_path)|`nvarchar(254)` |Path to the linked file. NULL when the file is embedded|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Document_File_Id](#document_file_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Embedded_File_Contents](#embedded_file_contents)|`varbinary` |The contents of the embedded file. NULL when the file is linked|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### File_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Is_Linked

| Property | Value |
| - | - |
|Type|bit|

### Linked_File_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Document_File_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Embedded_File_Contents

| Property | Value |
| - | - |
|Type|varbinary|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


