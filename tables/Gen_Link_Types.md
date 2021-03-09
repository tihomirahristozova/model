# Table Gen_Link_Types

Obsolete. Not used. Entity: Gen_Link_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` |Unique Id of the link type|
|[Code](#code)|`nvarchar(16)` `PK`|Unique link type code|
|[Link_Type_Name](#link_type_name)|`nvarchar(254)` |Obsolete. Not used.|
|[From_Doc_Type_Id](#from_doc_type_id)|`uniqueidentifier` |From which type of documents the link originates. NULL means that it might originate from any document type|
|[To_Doc_Type_Id](#to_doc_type_id)|`uniqueidentifier` |To what type of documents the link points. NULL means that it might point to any document type|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Link_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### From_Doc_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Doc_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


