# Table Gen_Product_Document_Amounts

Contains custom percent ratios for additional amount distribution over products. Entity: Gen_Product_Document_Amounts

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Document_Amount_Id](#product_document_amount_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The amount type for which the custom percent is defined.|
|[Line_Percent](#line_percent)|`decimal(14, 3)` |The custom percent for the current product and amount type.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Document_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Percent

| Property | Value |
| - | - |
|Type|decimal(14, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


