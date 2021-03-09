# Table Gen_Report_Queries

Contains the sub-queries, which a report contains. Entity: Gen_Report_Queries

## Owner Tables Hierarchy

* [Gen_Reports](Gen_Reports.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Report_Query_Id](#report_query_id)|`uniqueidentifier` `PK`||
|[Report_Id](#report_id)|`uniqueidentifier` ||
|[Reference_Path](#reference_path)|`nvarchar(512)` |A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document.|
|[Unique_Name](#unique_name)|`nvarchar(64)` |The name of the data table in the printout datasource. If NULL the Reference_Path is used.|
|[Show_Text_Columns](#show_text_columns)|`bit` |True to include text descriptions for certain columns.|
|[Show_Custom_Properties](#show_custom_properties)|`bit` |True to include the custom properties.|
|[Filter_Xml](#filter_xml)|`nvarchar(2147483647)` |Filter for the loaded table|
|[Table_Name](#table_name)|`nvarchar(64)` |The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be NULL.|
|[Depends_On_Child_Rows](#depends_on_child_rows)|`bit` |If True the data in the current report table contains only the rows that have child rows in sub-tables.|
|[Extensions_List](#extensions_list)|`nvarchar(2147483647)` |A comma separated list of report extension names. An extension is set of additional fields that participate in the query|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Report_Query_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Path

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Unique_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Show_Text_Columns

| Property | Value |
| - | - |
|Type|bit|

### Show_Custom_Properties

| Property | Value |
| - | - |
|Type|bit|

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
|Type|bit|

### Extensions_List

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


