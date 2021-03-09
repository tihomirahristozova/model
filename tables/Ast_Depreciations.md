# Table Ast_Depreciations

Depreciation documents contain actual depreciation values for one or more assets for one period. Entity: Ast_Depreciations

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Id](#depreciation_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Start_Date](#start_date)|`datetime` |Start date of the depreciation period accounted with this document|
|[End_Date](#end_date)|`datetime` |End date of the depreciation period accounted with this document|
|[Depreciation_Range](#depreciation_range)|`nvarchar(1)` Allowed: `A`, `S`|Determines whether all assets in the system will be depreciated or only the assets specified in the current document will be depreciated. A = 'All assets', S = 'Specified assets'|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Depreciation_Range

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


