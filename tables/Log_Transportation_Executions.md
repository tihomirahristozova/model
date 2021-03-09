# Table Log_Transportation_Executions

Contains executions (loading, unloading or other operations) of the transportation orders. Entity: Log_Transportation_Executions (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Execution_Id](#transportation_execution_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Execution_Date](#execution_date)|`date` |Specifies the execution date, if it is the same for all lines. NULL means that the lines have different execution dates.|
|[Execution_Time](#execution_time)|`time` |Specifies the execution time, if it is the same for all lines. NULL means that the lines have different execution times.|
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |Specifies the execution geographic point, if it is the same for all lines. NULL means that the lines have different geographic points.|

## Columns

### Transportation_Execution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Execution_Date

| Property | Value |
| - | - |
|Type|date|

### Execution_Time

| Property | Value |
| - | - |
|Type|time|

### Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


