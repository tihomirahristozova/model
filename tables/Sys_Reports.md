# Table Sys_Reports

User-defined reports. Reports retrieve data from data sources and present it in a user-defined layout. Entity: Sys_Reports

## Summary

| Name | Type | Description |
| - | - | --- |
|[Report_Id](#report_id)|`uniqueidentifier` `PK`||
|[Report_Name](#report_name)|`nvarchar(254)` |Multi-language report name|
|[Query_Name](#query_name)|`nvarchar(128)` |The query on which the report is based|
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` |Report data source. If specified should be based on the query in Query_Name. NULL means that the report is based directly on the query|
|[Report_Layout](#report_layout)|`nvarchar(2147483647)` |The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout|
|[Template_Filter_Xml](#template_filter_xml)|`nvarchar(2147483647)` |Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. NULL when the current report cannot be used as template sub-report.|
|[Template_Priority](#template_priority)|`int` |Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, NULL otherwise.|
|[One_Row](#one_row)|`bit` |True means that report can be used for one-row forms only. False means that the report can be used for navigators only.|
|[Notes](#notes)|`nvarchar(512)` ||
|[Layout_Format](#layout_format)|`nvarchar(32)` |Format specifier of the layout. Recognized by the application|
|[Report_Binary_Layout](#report_binary_layout)|`varbinary` |The printout layout, when the format requires binary storage. Alternative to Report_Layout|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Report_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Query_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Report_Layout

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Template_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Template_Priority

| Property | Value |
| - | - |
|Type|int|

### One_Row

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Layout_Format

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Report_Binary_Layout

| Property | Value |
| - | - |
|Type|varbinary|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


