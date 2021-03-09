# Table Gen_Document_Amount_Referenced_Documents

Contains the documents which are referenced by each document amount. Entity: Gen_Document_Amount_Referenced_Documents

## Owner Tables Hierarchy

* [Gen_Document_Amounts](Gen_Document_Amounts.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Referenced_Document_Id](#document_amount_referenced_document_id)|`uniqueidentifier` `PK`||
|[Document_Amount_Id](#document_amount_id)|`uniqueidentifier` |The document amount for which the referenced document is specified.|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |The document which is referenced by the document amount.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


