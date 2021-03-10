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


Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sys_Reports](Sys_Reports.md).[Report_Id](Sys_Reports.md#report_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Report_Name


Report_Name


Multi-language report name


Multi-language report name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Report_Name](Sys_Reports.md#report_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Query_Name


Query_Name


The query on which the report is based


The query on which the report is based

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Query_Name](Sys_Reports.md#query_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Data_Source_Id


Data_Source_Id


Report data source. If specified should be based on the query in Query_Name. NULL means that the report is based directly on the query


Report data source. If specified should be based on the query in Query_Name. NULL means that the report is based directly on the query

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Data_Sources](Sys_Data_Sources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Data_Source_Id](Sys_Reports.md#data_source_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Report_Layout


Report_Layout


The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout


The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Report_Layout](Sys_Reports.md#report_layout)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Template_Filter_Xml


Template_Filter_Xml


Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. NULL when the current report cannot be used as template sub-report.


Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. NULL when the current report cannot be used as template sub-report.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Template_Filter_Xml](Sys_Reports.md#template_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Template_Priority


Template_Priority


Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, NULL otherwise.


Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, NULL otherwise.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Template_Priority](Sys_Reports.md#template_priority)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### One_Row


One_Row


True means that report can be used for one-row forms only. False means that the report can be used for navigators only.


True means that report can be used for one-row forms only. False means that the report can be used for navigators only.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sys_Reports](Sys_Reports.md).[One_Row](Sys_Reports.md#one_row)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Notes](Sys_Reports.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|512|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Layout_Format


Layout_Format


Format specifier of the layout. Recognized by the application


Format specifier of the layout. Recognized by the application

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Layout_Format](Sys_Reports.md#layout_format)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Report_Binary_Layout


Report_Binary_Layout


The printout layout, when the format requires binary storage. Alternative to Report_Layout


The printout layout, when the format requires binary storage. Alternative to Report_Layout

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Report_Binary_Layout](Sys_Reports.md#report_binary_layout)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Reports](Sys_Reports.md).[Row_Version](Sys_Reports.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


