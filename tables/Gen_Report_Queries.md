# Table Gen_Report_Queries

Contains the sub-queries, which a report contains. Entity: Gen_Report_Queries

# Aggregate Hierarchy

* [Gen_Reports](Gen_Reports.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Report_Query_Id|`Guid`|`PK`, Readonly||
|Depends_On_Child_Rows|`Boolean`||If True the data in the current report table contains only the rows that have child rows in sub-tables. `Required` `Default(false)` |
|Extensions_List|`String`||A comma separated list of report extension names. An extension is set of additional fields that participate in the query. |
|Filter_Xml|`DataAccessFilter`||Filter for the loaded table. |
|Reference_Path|`String`||A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required` |
|Show_Custom_Properties|`Boolean`||True to include the custom properties. `Required` `Default(false)` |
|Show_Text_Columns|`Boolean`||True to include text descriptions for certain columns. `Required` `Default(false)` |
|Table_Name|`String`||The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. |
|Unique_Name|`String`||The name of the data table in the printout datasource. If null the Reference_Path is used. |
