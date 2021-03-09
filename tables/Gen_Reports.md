# Table Gen_Reports

Contains user-defined data-sources. The data sources is a user-defined way (similar to query designer) to extract, filter, join and transform data for presentation purposes. Entity: Gen_Reports

## Summary

| Name | Type | Description |
| - | - | --- |
|[Report_Id](#report_id)|`uniqueidentifier` `PK`||
|[Report_Name](#report_name)|`nvarchar(64)` ||
|[Query_Name](#query_name)|`nvarchar(128)` |The name of the query or table that is used for root reference point of the loaded data.|
|[Is_Table](#is_table)|`bit` |If True the Query_Name is name of a table, otherwise is name of a query that can be filtered with Filter_Xml. |
|[Show_Parent_Tables](#show_parent_tables)|`bit` |Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Report_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Query_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Is_Table

| Property | Value |
| - | - |
|Type|bit|

### Show_Parent_Tables

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


