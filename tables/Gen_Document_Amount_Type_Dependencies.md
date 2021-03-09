# Table Gen_Document_Amount_Type_Dependencies

Specifies the base amounts on which an amount depends. . Entity: Gen_Document_Amount_Type_Dependencies

## Owner Tables Hierarchy

* [Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Dependency_Id](#document_amount_type_dependency_id)|`uniqueidentifier` `PK`||
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The amount for which the base amount is specified.|
|[Depends_On_Document_Amount_Type_Id](#depends_on_document_amount_type_id)|`uniqueidentifier` |The base amount type on which the current amount depends.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Type_Dependency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depends_On_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


