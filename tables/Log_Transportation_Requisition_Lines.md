# Table Log_Transportation_Requisition_Lines

One line in a client requisition for transportation. Different lines usually represent requisitions for different cargo types. Entity: Log_Transportation_Requisition_Lines

## Owner Tables Hierarchy

* [Log_Transportation_Requisitions](Log_Transportation_Requisitions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Requisition_Line_Id](#transportation_requisition_line_id)|`uniqueidentifier` `PK`||
|[Transportation_Requisition_Id](#transportation_requisition_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |The type of the transported cargo.|
|[Contents_Description](#contents_description)|`nvarchar(128)` |Textual description of the cargo contents.|
|[Weight_Kg](#weight_kg)|`int` |The weight of the cargo, in KG (kilogramms). NULL when it is unknown.|
|[Volume_Cbm](#volume_cbm)|`int` |The volume of the cargo, in CBM (cubic meters). NULL when it is unknown.|
|[Pallets_Count](#pallets_count)|`int` |Number of palettes comprising the cargo. NULL when it is unknown.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute another line.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transportation_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Cargo_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contents_Description

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Weight_Kg

| Property | Value |
| - | - |
|Type|int|

### Volume_Cbm

| Property | Value |
| - | - |
|Type|int|

### Pallets_Count

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


