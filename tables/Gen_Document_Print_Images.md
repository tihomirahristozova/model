# Table Gen_Document_Print_Images

Contains the data of a printout of a document as it was obtained from the data source in the moment of printing. Entity: Gen_Document_Print_Images

## Owner Tables Hierarchy

* [Gen_Printout_Layouts](Gen_Printout_Layouts.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Print_Image_Id](#document_print_image_id)|`uniqueidentifier` `PK`||
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` |The print layout, which was used for the current printout.|
|[Print_Image_Format](#print_image_format)|`nvarchar(3)` |The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported.|
|[Print_Image](#print_image)|`varbinary` |The data of the printout, stored in the format, specified in Print Image Format.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Print_Image_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Printout_Layout_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Print_Image_Format

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Print_Image

| Property | Value |
| - | - |
|Type|varbinary|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


