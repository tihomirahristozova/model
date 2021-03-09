# Table Gen_Document_Line_Amounts

Specifies user-defined distribution pattern of additonal amount for specific document. Entity: Gen_Document_Line_Amounts

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Line_Amount_Id](#document_line_amount_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Line_Id](#document_line_id)|`uniqueidentifier` |The line for which the distribution pattern is specified.|
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The type of amount for which the distribution pattern is specified.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which the distribution is specified. It is also the product, specified in the document line, but is duplicated here for integrity purposes.|
|[Line_Percent](#line_percent)|`decimal(14, 6)` |The percent of the additional amount which should be distributed over the current line.|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |When not null, specifies that this distribution is specified for a referenced document (not the document for which the amount is calculated).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Line_Amount_Id

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

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Percent

| Property | Value |
| - | - |
|Type|decimal(14, 6)|

### Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


