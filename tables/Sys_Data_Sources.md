# Table Sys_Data_Sources

Contains user-defined data sources, which retrieve rows from multiple queries. Entity: Sys_Data_Sources

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` `PK`||
|[Data_Source_Name](#data_source_name)|`nvarchar(64)` |The name of the data source.|
|[Base_Query_Name](#base_query_name)|`nvarchar(128)` |The name of the query or table that is used for root reference point of the loaded data.|
|[Show_Parent_Tables](#show_parent_tables)|`bit` |Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not.|
|[Data_Source_Type](#data_source_type)|`nvarchar(1)` Allowed: `M`, `D`, `S`|'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE |
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Source_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Base_Query_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Show_Parent_Tables

| Property | Value |
| - | - |
|Type|bit|

### Data_Source_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


