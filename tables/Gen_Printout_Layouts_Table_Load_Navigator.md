# Query Gen_Printout_Layouts_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` `PK`||
|[Printout_Layout_Name](#printout_layout_name)|`nvarchar` ||
|[Document_Entity_Name](#document_entity_name)|`nvarchar` |The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc.|
|[Layout](#layout)|`nvarchar` |The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout|
|[Layout_Format](#layout_format)|`nvarchar` |Format specifier of the layout. Recognized by the application|
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` |The data source for the printout|
|[Notes](#notes)|`nvarchar` ||
|[Binary_Layout](#binary_layout)|`varbinary` ||

## Columns

### Printout_Layout_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Printout_Layout_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Layout

| Property | Value |
| - | - |
|Type|nvarchar|

### Layout_Format

| Property | Value |
| - | - |
|Type|nvarchar|

### Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Binary_Layout

| Property | Value |
| - | - |
|Type|varbinary|


