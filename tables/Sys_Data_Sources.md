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


Data_Source_Id

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
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Data_Source_Id](Sys_Data_Sources.md#data_source_id)|
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

### Data_Source_Name


Data_Source_Name


The name of the data source.


The name of the data source.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Data_Source_Name](Sys_Data_Sources.md#data_source_name)|
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
|Max Length|64|
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

### Base_Query_Name


Base_Query_Name


The name of the query or table that is used for root reference point of the loaded data.


The name of the query or table that is used for root reference point of the loaded data.

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
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Base_Query_Name](Sys_Data_Sources.md#base_query_name)|
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
|Equals|NULL|no|yes|
|Like|None|no|no|

### Show_Parent_Tables


Show_Parent_Tables


Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not.


Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not.

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
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Show_Parent_Tables](Sys_Data_Sources.md#show_parent_tables)|
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

### Data_Source_Type


Data_Source_Type


'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE 


'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE 

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`M`, `D`, `S`|
|Default Value|M|
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Data_Source_Type](Sys_Data_Sources.md#data_source_type)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Sys_Data_Sources](Sys_Data_Sources.md).[Row_Version](Sys_Data_Sources.md#row_version)|
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


