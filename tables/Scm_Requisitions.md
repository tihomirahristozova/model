# Table Scm_Requisitions

Contains the internal requisitions for products. Requisitions are consolidated by the purchase department into purchase orders. Entity: Scm_Requisitions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Requisition_Id](#requisition_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` |The store in which the products are needed.|
|[Requested_By_Party_Id](#requested_by_party_id)|`uniqueidentifier` |The party, which is requesting the purchase order.|
|[Required_Delivery_Date](#required_delivery_date)|`datetime` |When not null, specifies the required delivery date for all lines.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requested_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

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


