# Table Gen_Printout_Layouts

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` `PK`||
|[Printout_Layout_Name](#printout_layout_name)|`nvarchar(64)` ||
|[Document_Entity_Name](#document_entity_name)|`nvarchar(64)` |The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc.|
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` |The data source for the printout|
|[Layout](#layout)|`nvarchar(2147483647)` |The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout|
|[Layout_Format](#layout_format)|`nvarchar(32)` |Format specifier of the layout. Recognized by the application|
|[Notes](#notes)|`nvarchar(254)` ||
|[Binary_Layout](#binary_layout)|`varbinary` |The printout layout, when the format requires binary storage. Alternative to Layout|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Printout_Layout_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Printout_Layout_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Document_Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Layout

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Layout_Format

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Binary_Layout

| Property | Value |
| - | - |
|Type|varbinary|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


