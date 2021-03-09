# Table Crm_Offers_Options

Contains options for user defined document types for Offers. Entity: Crm_Offers_Options

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Offer_Option_Id](#offer_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the offer option applies.|
|[Deal_Document_Type_Id](#deal_document_type_id)|`uniqueidentifier` |If filled then new opportunities (deals) from the specified type will be created automatically for the offers that aren't assigned to existing opportunities. Used for automating opportunity management.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Offer_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


