# Table Gen_Document_Versions

History of each saved version of each document. Entity: Gen_Document_Versions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Version_Id](#document_version_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document whoose version is stored in this row|
|[Version](#version)|`int` Readonly|The version number that is stored in this row|
|[Document_Data_XML](#document_data_xml)|`nvarchar(2147483647)` |The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed).|
|[Update_Time](#update_time)|`datetime` Readonly|The date and time when this version was saved|
|[Update_User](#update_user)|`nvarchar(64)` Readonly|The login name of the user that saved this version|
|[State](#state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`, Readonly|The state of the document by the time it was saved|
|[Document_Data_Format](#document_data_format)|`nvarchar(1)` |The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data.|
|[Document_Data](#document_data)|`varbinary` |Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Version_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Version

| Property | Value |
| - | - |
|Type|int|

### Document_Data_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Document_Data_Format

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Document_Data

| Property | Value |
| - | - |
|Type|varbinary|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


