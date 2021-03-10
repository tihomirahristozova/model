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


Data_Source_Query_Id

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
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Data_Source_Query_Id](Sys_Data_Source_Queries.md#data_source_query_id)|
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
|Equals|NULL|no|no|

### Data_Source_Id


Data_Source_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Data_Sources](Sys_Data_Sources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Data_Source_Id](Sys_Data_Source_Queries.md#data_source_id)|
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
|Equals|NULL|no|no|

### Reference_Path


Reference_Path


A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document.


A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Reference_Path](Sys_Data_Source_Queries.md#reference_path)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Unique_Name


Unique_Name


The name of the data table in the printout datasource. If NULL the Reference_Path is used.


The name of the data table in the printout datasource. If NULL the Reference_Path is used.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Unique_Name](Sys_Data_Source_Queries.md#unique_name)|
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
|Visible|no|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Filter_Xml


Filter_Xml


Filter for the loaded table


Filter for the loaded table

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
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Filter_Xml](Sys_Data_Source_Queries.md#filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Table_Name


Table_Name


The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be NULL.


The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be NULL.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Table_Name](Sys_Data_Source_Queries.md#table_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Depends_On_Child_Rows


Depends_On_Child_Rows


Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows


Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `1`, `2`|
|Default Value|0|
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Depends_On_Child_Rows](Sys_Data_Source_Queries.md#depends_on_child_rows)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Extensions_List


Extensions_List


A comma separated list of report extension names. An extension is set of additional fields that participate in the query


A comma separated list of report extension names. An extension is set of additional fields that participate in the query

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
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Extensions_List](Sys_Data_Source_Queries.md#extensions_list)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### First_Row


First_Row


Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable.


Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable.

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
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[First_Row](Sys_Data_Source_Queries.md#first_row)|
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
|Derived From|[Sys_Data_Source_Queries](Sys_Data_Source_Queries.md).[Row_Version](Sys_Data_Source_Queries.md#row_version)|
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


