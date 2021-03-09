# Table Cost_Distributions

Used for cost distribution. Contains the period and the store of the cost distribution. Entity: Cost_Distributions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Start_Date](#start_date)|`date` |The starting date of the covered period.|
|[End_Date](#end_date)|`date` |The ending date of the covered period.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store (warehouse) for which the distribution is made. NULL means that the distribution covers multiple warehouses.|

## Columns

### Cost_Distribution_Id

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
|Type|date|

### End_Date

| Property | Value |
| - | - |
|Type|date|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


