# Table Sys_Data_Source_Queries

Represents a query within a data source. Entity: Sys_Data_Source_Queries

## Owner Tables Hierarchy

* [Sys_Data_Sources](Sys_Data_Sources.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Source_Query_Id](#data_source_query_id)|`uniqueidentifier` `PK`||
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` ||
|[Reference_Path](#reference_path)|`nvarchar(2147483647)` |A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document.|
|[Unique_Name](#unique_name)|`nvarchar(64)` |The name of the data table in the printout datasource. If NULL the Reference_Path is used.|
|[Filter_Xml](#filter_xml)|`nvarchar(2147483647)` |Filter for the loaded table|
|[Table_Name](#table_name)|`nvarchar(64)` |The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be NULL.|
|[Depends_On_Child_Rows](#depends_on_child_rows)|`tinyint` Allowed: `0`, `1`, `2`|Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows|
|[Extensions_List](#extensions_list)|`nvarchar(2147483647)` |A comma separated list of report extension names. An extension is set of additional fields that participate in the query|
|[First_Row](#first_row)|`bit` |Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Data_Source_Query_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Path

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Unique_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Table_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Depends_On_Child_Rows

| Property | Value |
| - | - |
|Type|tinyint|

### Extensions_List

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### First_Row

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


