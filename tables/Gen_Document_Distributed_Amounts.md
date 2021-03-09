# Table Gen_Document_Distributed_Amounts

Contains the amounts which are distributed by the system over the document lines as a result of additional amount calculations. Entity: Gen_Document_Distributed_Amounts

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Distributed_Amount_Id](#distributed_amount_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Line_Id](#document_line_id)|`uniqueidentifier` |The Id of the line over which the amount is distributed.|
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The type of amount which is distributed.|
|[Amount](#amount)|`decimal(14, 2)` |The amount which has beed distributed over the current line. The amount is in the currency of the document.|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |In not null the Document_Line_Id is a line of the document with Referenced_Document_Id|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Distributed_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


