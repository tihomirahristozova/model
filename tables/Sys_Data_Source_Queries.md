# Table Sys_Data_Source_Queries

Represents a query within a data source. Entity: Sys_Data_Source_Queries

# Aggregate Hierarchy

* [Sys_Data_Sources](Sys_Data_Sources.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Source_Query_Id|`Guid`|`PK`, Readonly||
|Depends_On_Child_Rows|`DependsOnChildRows`|Allowed: `0`, `1`, `2`|Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows. `Required` `Default(0)` |
|Extensions_List|`String`||A comma separated list of report extension names. An extension is set of additional fields that participate in the query. |
|Filter_Xml|`DataAccessFilter`||Filter for the loaded table. |
|First_Row|`Boolean`||Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable. `Required` `Default(false)` |
|Reference_Path|`String`||A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required` |
|Table_Name|`String`||The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. |
|Unique_Name|`String`||The name of the data table in the printout datasource. If null the Reference_Path is used. |
